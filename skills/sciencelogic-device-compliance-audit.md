---
name: sciencelogic-device-compliance-audit
description: Audit a fleet of network devices for compliance-policy violations using the ScienceLogic Skylar Compliance API, and report which devices fail which policies.
api: Skylar Compliance API 2.0
base_url: https://{appliance}/api/v2
operations:
  - list_domains
  - list_devices
  - list_policies
  - get_policy
  - device_compliance
generated: '2026-08-29'
method: generated
source: openapi/sciencelogic-skylar-compliance-openapi.json
---

# Audit device compliance with Skylar Compliance

Read-only. Every operation in this skill is a GET. Nothing here changes device state.

## Before you start

- The base URL is the customer's own appliance: `https://{appliance}/api/v2`. There is no vendor-hosted
  host — ask for the appliance hostname; never guess one.
- Authenticate with a token minted in the Skylar Compliance web interface, sent as
  `Authorization: Custom <token>`. Session cookies are for the product UI, not for you.
- Your token is scoped to one or more **domains**. A device you cannot see returns `404`, not `403`.
  If a device id you were given returns 404, check domain scope before concluding it does not exist.
- Required permissions: `ViewDomain`, `ViewDevices`, `ViewDevicePolicy`. A `403` means the role behind
  your token is missing one of them — say which, do not retry.

## Steps

1. **Establish scope.** `GET /domains` (`list_domains`) to learn which domains your token can see. If the
   user named a domain, resolve it to a `DomainID` here rather than assuming.

2. **List the fleet.** `GET /devices` (`list_devices`), filtering by `domain_id[]` when scoped.
   Pagination is offset/limit: `limit` defaults to 50 and is capped at 500, and every list response
   carries `total`, so compute the number of pages up front instead of walking until empty. Use
   `fields=ID,Name,DomainID` to keep responses small.

3. **List the policies.** `GET /policies` (`list_policies`). For any policy the user asked about, read
   `GET /policies/{id}` (`get_policy`) to get its rules and description so your report can say what the
   device actually violated, not just that it failed.

4. **Test each device.** `GET /devices/{id}/compliance` (`device_compliance`) returns that device's
   compliance results. Call it per device — there is no bulk endpoint.

5. **Report.** Group by policy, then by device. For each violation quote the policy name and rule so the
   operator can act without a second lookup.

## Failure handling

- `400` — the response body is `{ "message": ..., "errors": { "<field>": ["<msg>"] } }`. Fix the named
  field; retrying unchanged fails identically.
- `401` — the token is missing, malformed or rejected. The error body may also carry `EncryptionStatus`;
  if it is `Decrypting` the appliance is still coming up after a restart, and a `503` follows until it
  finishes. That case is retryable with backoff.
- `403` — missing permission. Name the permission from the operation's `Permissions` list.
- `404` — bad id **or** domain scope. Re-resolve, do not retry.
- `500` / `503` / `504` — retry once with backoff, then stop and report.

## Do not

- Do not call `/devices/{id}/backups/{backup_id}/restore`, `/policies/{id}/test`, or any DELETE. This
  skill is an audit, not a remediation.
- There are no idempotency keys on this API. If you ever move beyond reads, treat every write as
  at-most-once.
