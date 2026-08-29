---
name: sciencelogic-appliance-health-triage
description: Triage the health of a ScienceLogic Skylar Compliance appliance — HA status, running and historic jobs, agents and system logs — to answer "is this thing healthy and what is it doing right now".
api: Skylar Compliance API 2.0
base_url: https://{appliance}/api/v2
operations:
  - system_status
  - get_high_availability_status
  - list_agents
  - list_jobs
  - list_historic_jobs
  - get_job
  - list_logs
generated: '2026-08-29'
method: generated
source: openapi/sciencelogic-skylar-compliance-openapi.json
---

# Triage a Skylar Compliance appliance

Read-only. This mirrors the `status`, `list_agents`, `list_jobs`, `list_historic_jobs` and `list_logs`
tools in the ScienceLogic MCP server, and is the skill to reach for when someone asks whether the
platform itself is the problem.

## Before you start

- Base URL: `https://{appliance}/api/v2`. There is no ScienceLogic status page to check first — the
  appliance is the customer's own, so this API **is** the status surface.
- Auth: `Authorization: Custom <token>`. Permissions: `ViewSysadmin`, `ViewDevices`, `ViewLogs`.

## Steps

1. **Appliance health.** `GET /status` (`system_status`).

2. **Cluster health.** `GET /settings/ha/status` (`get_high_availability_status`). Only meaningful on
   Advanced (H/A) licences; on a single appliance report it as not applicable rather than as a failure.

3. **Collection reach.** `GET /agents` (`list_agents`). A disconnected agent explains a whole class of
   "device stopped backing up" reports. Agents chain — `SecondaryToAgentID` points at the parent — so a
   failure upstream takes its children with it.

4. **What is running now.** `GET /jobs` (`list_jobs`).

5. **What just finished.** `GET /jobs/historic` (`list_historic_jobs`), newest first. `GET /jobs/{id}`
   (`get_job`) for detail on any failure.

6. **Logs.** `GET /logs` (`list_logs`) for appliance activity. `GET /syslogs` is a separate, device-facing
   collection — do not confuse the two.

## Interpreting failures

- A `503` with `EncryptionStatus: Decrypting` means the appliance restarted and is still decrypting its
  disk. That is the answer, not an error — report it and retry with backoff.
- `EncryptionStatus: Failure` means decryption failed. Stop and escalate; nothing else will work.
- The platform separately throttles inbound syslog/SNMP-trap floods at 25 messages/second per source IP
  and raises a Critical "Inbound Message Flood" event. If a device's data went quiet, check for that
  event before blaming the API.

## Pagination

`offset` (default 0) and `limit` (default 50, max 500), with `total` in every list envelope. Use
`sort=-Date` for the job and log lists.
