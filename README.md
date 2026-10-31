# ScienceLogic

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

ScienceLogic is an AIOps and IT operations company whose ScienceLogic AI Platform — rebranded in 2026 as the Skylar family — covers infrastructure and application observability, network configuration and compliance, and workflow automation. Skylar One (formerly SL1) is the observability platform, with a REST API and a GraphQL API served from the customer's own Administration Portal, All-In-One Appliance or Database Server; ScienceLogic states that GraphQL is the forward path and that the REST API is now limited to bug fixes. Skylar Compliance (formerly Restorepoint, acquired by ScienceLogic) publishes a 314-operation OpenAPI 3.0 contract for configuration backup, change detection, compliance policy testing and device restore. Skylar Automation (formerly PowerFlow) handles ITSM and CMDB integration, and Skylar AI adds Advisor and Analytics on top. The ScienceLogic GitHub organization also publishes an MCP server that exposes read-only Skylar One and Skylar Compliance tools to AI agents. Products are deployed on customer appliances, SaaS, or private/public cloud, and are licensed per managed device per month.

**Areas:** AIOps · IT Operations · Observability · Monitoring · Network Configuration Management · Compliance · Automation · Incident Management

## ScienceLogic on APIs.io

Everything profiled for ScienceLogic is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/sciencelogic/](https://apis.io/providers/sciencelogic/)** — or go straight to one of the APIs or properties below.

### APIs (80)

- [ScienceLogic](https://apis.io/apis/sciencelogic/sciencelogic/) — The ScienceLogic AI Platform (Skylar) — AIOps, IT infrastructure and application observability, service management, network configuration compliance, and…
- [Skylar One GraphQL API](https://apis.io/apis/sciencelogic/skylar-one-graphql-api/) — The GraphQL API for Skylar One (formerly SL1). ScienceLogic's forward-looking interface — the default AP2 user interface uses it exclusively and makes no…
- [Skylar One REST API](https://apis.io/apis/sciencelogic/skylar-one-rest-api/) — The REST API for Skylar One (formerly SL1), giving external systems programmatic access to tickets, devices, organizations, events, monitoring policies,…
- [ScienceLogic MCP Server](https://apis.io/apis/sciencelogic/sciencelogic-mcp/) — A FastMCP server published by the ScienceLogic GitHub organization exposing 22 read-only tools across two sub-servers — Skylar One (backed by the SL1…
- [ScienceLogic Agent API](https://apis.io/apis/sciencelogic/sciencelogic-agent-api/) — Agents allow a Skylar Compliance appliance to manage devices located on a remote or otherwise disjointed network, not directly routable by Skylar…
- [ScienceLogic Agent/Debug API](https://apis.io/apis/sciencelogic/sciencelogic-agent-debug-api/) — Endpoints that can aid in debugging agent problems.
- [ScienceLogic Agent/Remote API](https://apis.io/apis/sciencelogic/sciencelogic-agent-remote-api/) — Start and stop remote support access on agents.
- [ScienceLogic Backup API](https://apis.io/apis/sciencelogic/sciencelogic-backup-api/) — A device backup can encapsulates one or more device configurations. Depending on the type of device, a device backup might be a simple text file or a…
- [ScienceLogic Command API](https://apis.io/apis/sciencelogic/sciencelogic-command-api/) — Skylar Compliance allows you to send a CLI command to a device or group of devices and capture the output of the command. This is a very convenient tool to…
- [ScienceLogic Command/Output API](https://apis.io/apis/sciencelogic/sciencelogic-command-output-api/) — Logs from running [scheduled commands](#tag/CommandSchedule) with `StoreLog` enabled can be retrieved here.
- [ScienceLogic Command/Schedule API](https://apis.io/apis/sciencelogic/sciencelogic-command-schedule-api/) — Commands can be scheduled to run automatically at defined intervals or once.
- [ScienceLogic Command/Variables API](https://apis.io/apis/sciencelogic/sciencelogic-command-variables-api/) — Commands can have one or multiple variables. The user can upload a csv file with a list of variables and they will be parsed and used when running the command.
- [ScienceLogic Credential API](https://apis.io/apis/sciencelogic/sciencelogic-credential-api/) — Set of username and up to two passwords that can be used across multiple devices.
- [ScienceLogic Credential/Bulk API](https://apis.io/apis/sciencelogic/sciencelogic-credential-bulk-api/) — Allows creating or updating multiple credentials at once. It will create a scheduled task with the given credentials and create a log entry for the…
- [ScienceLogic Credential/Provider/Cyber Ark API](https://apis.io/apis/sciencelogic/sciencelogic-credential-provider-cyberark-api/) — Allows retrieving credentials from the external vault.
- [ScienceLogic Device API](https://apis.io/apis/sciencelogic/sciencelogic-device-api/) — Devices are Skylar Compliance's representation of physical or virtual network devices.
- [ScienceLogic Device/Backup API](https://apis.io/apis/sciencelogic/sciencelogic-device-backup-api/) — A device backup can encapsulates one or more device configurations. Depending on the type of device, a device backup might be a simple text file or a…
- [ScienceLogic Device/Bulk Create API](https://apis.io/apis/sciencelogic/sciencelogic-device-bulkcreate-api/) — Allows creating multiple devices at once. It will create a scheduled task with the given devices and create a log entry for each device creation and one…
- [ScienceLogic Device/Bulk Edit API](https://apis.io/apis/sciencelogic/sciencelogic-device-bulkedit-api/) — Allows editing multiple devices at once. This losely follows the structure of the [Device](#tag/Device) model. Skylar Compliance will aggregate values for…
- [ScienceLogic Dictionary API](https://apis.io/apis/sciencelogic/sciencelogic-dictionary-api/) — Dictionaries for various auto-complete and search filter settings.
- [ScienceLogic Discovery API](https://apis.io/apis/sciencelogic/sciencelogic-discovery-api/) — The Skylar Compliance device discovery engine uses a variety of methods to discover hosts on your network that can be imported into the main device list.…
- [ScienceLogic Discovery/Device API](https://apis.io/apis/sciencelogic/sciencelogic-discovery-device-api/) — New devices as discovered by a manual or scheduled device discovery run will appear here.
- [ScienceLogic Domain API](https://apis.io/apis/sciencelogic/sciencelogic-domain-api/) — Domains allow you to organise devices into separate domains, and delegate their management to Domain Administrators. A typical use is for Service Providers…
- [ScienceLogic Download API](https://apis.io/apis/sciencelogic/sciencelogic-download-api/) — An endpoint to download files from.
- [ScienceLogic Export API](https://apis.io/apis/sciencelogic/sciencelogic-export-api/) — Allows you to export device configurations, logs and settings for multiple devices or domains.
- [ScienceLogic Export/Policy API](https://apis.io/apis/sciencelogic/sciencelogic-export-policy-api/) — Automatically export device configurations to a specified file server. Please do not mistake this for the [device policy…
- [ScienceLogic Firmware API](https://apis.io/apis/sciencelogic/sciencelogic-firmware-api/) — Skylar Compliance can act as a repository for device firmware/software, allowing you to upload files like firmware images and ISO images to the appliance.…
- [ScienceLogic Job API](https://apis.io/apis/sciencelogic/sciencelogic-job-api/) — Jobs represent a running task in Skylar Compliance, such as a running device backup, command or creating an archive of Skylar Compliance. Normally, a job…
- [ScienceLogic Label API](https://apis.io/apis/sciencelogic/sciencelogic-label-api/) — Labels are a way of attaching meta information to devices. They allow for arbitrary grouping and selection of devices that can go beyond the use of device…
- [ScienceLogic Log API](https://apis.io/apis/sciencelogic/sciencelogic-log-api/) — Almost every system activity will be logged and can be retrieved
- [ScienceLogic Login API](https://apis.io/apis/sciencelogic/sciencelogic-login-api/) — The login endpoint is used by the UI to authenticate a user. On successful login, it will set a session cookie that will further authenticate API requests…
- [ScienceLogic Network API](https://apis.io/apis/sciencelogic/sciencelogic-network-api/) — Network utility endpoints.
- [ScienceLogic Permission API](https://apis.io/apis/sciencelogic/sciencelogic-permission-api/) — Permissions are the building blocks of what a user's role is entitled to perform. Permissions are read-only.
- [ScienceLogic Permissions/Validate Request API](https://apis.io/apis/sciencelogic/sciencelogic-permissions-validaterequest-api/) — The Permissions/ValidateRequest API from ScienceLogic — 1 operation(s) for permissions/validaterequest.
- [ScienceLogic Plugin API](https://apis.io/apis/sciencelogic/sciencelogic-plugin-api/) — Plugins have a number of device specific settings that are required for creating a functional device configurations for backup, restore or running commands.
- [ScienceLogic Plugin default values API](https://apis.io/apis/sciencelogic/sciencelogic-plugin-default-values-api/) — The Plugin default values API from ScienceLogic — 1 operation(s) for plugin default values.
- [ScienceLogic Plugin redact rule API](https://apis.io/apis/sciencelogic/sciencelogic-plugin-redact-rule-api/) — The Plugin redact rule API from ScienceLogic — 2 operation(s) for plugin redact rule.
- [ScienceLogic Policy API](https://apis.io/apis/sciencelogic/sciencelogic-policy-api/) — Skylar Compliance enables you to create policies that can be used to verify that your devices comply with corporate or regulatory guidelines. Policies are…
- [ScienceLogic Policy/Rule API](https://apis.io/apis/sciencelogic/sciencelogic-policy-rule-api/) — Rules are the individual parts of a device policy. ## Regular Expressions A regular expression specifies a set of strings as a pattern, rather than a list.…
- [ScienceLogic Policy/Variable API](https://apis.io/apis/sciencelogic/sciencelogic-policy-variable-api/) — Policy variables can be used in compliance rules as variable replacements, referenced with the `$replace$` format, where `replace` is the variable name you…
- [ScienceLogic Recovery API](https://apis.io/apis/sciencelogic/sciencelogic-recovery-api/) — The Recovery API from ScienceLogic — 2 operation(s) for recovery.
- [ScienceLogic Report API](https://apis.io/apis/sciencelogic/sciencelogic-report-api/) — The Report API from ScienceLogic — 4 operation(s) for report.
- [ScienceLogic Report schedule API](https://apis.io/apis/sciencelogic/sciencelogic-report-schedule-api/) — The Report schedule API from ScienceLogic — 2 operation(s) for report schedule.
- [ScienceLogic Role API](https://apis.io/apis/sciencelogic/sciencelogic-role-api/) — In addition to the standard built-in roles (`Admin`, `Backup`, and `View Only`), which cannot be edited, it is possible to define granular, custom roles,…
- [ScienceLogic SAML API](https://apis.io/apis/sciencelogic/sciencelogic-saml-api/) — The SAML API from ScienceLogic — 2 operation(s) for saml.
- [ScienceLogic Schedule API](https://apis.io/apis/sciencelogic/sciencelogic-schedule-api/) — Allows a view of the next occurence of all scheduled events including device backups, Skylar Compliance archival, device discovery as well as reporting.
- [ScienceLogic Settings/Advanced API](https://apis.io/apis/sciencelogic/sciencelogic-settings-advanced-api/) — The Settings/Advanced API from ScienceLogic — 1 operation(s) for settings/advanced.
- [ScienceLogic Settings/Alerts API](https://apis.io/apis/sciencelogic/sciencelogic-settings-alerts-api/) — Configure system email alert settings.
- [ScienceLogic Settings/Appliance/Actions API](https://apis.io/apis/sciencelogic/sciencelogic-settings-appliance-actions-api/) — Trigger global appliance actions.
- [ScienceLogic Settings/Appliance API](https://apis.io/apis/sciencelogic/sciencelogic-settings-appliance-api/) — Allows you to set general appliance settings as well as triggering global appliance actions.
- [ScienceLogic Settings/Appliance/Debug API](https://apis.io/apis/sciencelogic/sciencelogic-settings-appliance-debug-api/) — Endpoints that can aid in debugging appliance problems.
- [ScienceLogic Settings/Appliance/Logo API](https://apis.io/apis/sciencelogic/sciencelogic-settings-appliance-logo-api/) — Add, update or reset a custom logo for the appliance UI.
- [ScienceLogic Settings/Appliance/Support API](https://apis.io/apis/sciencelogic/sciencelogic-settings-appliance-support-api/) — Start and stop remote support sessions.
- [ScienceLogic Settings/Appliance/Updates API](https://apis.io/apis/sciencelogic/sciencelogic-settings-appliance-updates-api/) — Check, retrieve and update the appliance.
- [ScienceLogic Settings/Archive API](https://apis.io/apis/sciencelogic/sciencelogic-settings-archive-api/) — You can prepare for disaster recovery scenarios by archiving the Skylar Compliance configuration. This allows you to back up the Skylar Compliance appliance…
- [ScienceLogic Settings/Assetfield API](https://apis.io/apis/sciencelogic/sciencelogic-settings-assetfield-api/) — Configure device asset information fields including location, asset tag, and serial number.
- [ScienceLogic Settings/Assetfield/Notifications API](https://apis.io/apis/sciencelogic/sciencelogic-settings-assetfield-notifications-api/) — Configure device asset notify address.
- [ScienceLogic Settings/Authentication API](https://apis.io/apis/sciencelogic/sciencelogic-settings-authentication-api/) — Allows you to configure additional authentication methods for Skylar Compliance. Supported methods are: * RADIUS * SAML * LDAP
- [ScienceLogic Settings/Device API](https://apis.io/apis/sciencelogic/sciencelogic-settings-device-api/) — Allows you to set default device settings that are inherited whenever a new device is added but can be overriden.
- [ScienceLogic Settings/Discovery API](https://apis.io/apis/sciencelogic/sciencelogic-settings-discovery-api/) — Allows you to set device discovery settings for manual or scheduled device discovery runs.
- [ScienceLogic Settings/HA API](https://apis.io/apis/sciencelogic/sciencelogic-settings-ha-api/) — High Availability (HA) provides a way to minimise the effects of hardware failure, by configuring two Skylar Compliance appliances in a cluster. Under…
- [ScienceLogic Settings/Logs API](https://apis.io/apis/sciencelogic/sciencelogic-settings-logs-api/) — Allows you to configure default log rentention and other logging related settings.
- [ScienceLogic Settings/Network API](https://apis.io/apis/sciencelogic/sciencelogic-settings-network-api/) — Allows you to set network settings such as the IP address and static routes. ### Network Address Translation (NAT) Skylar Compliance may use…
- [ScienceLogic Settings/Passwords API](https://apis.io/apis/sciencelogic/sciencelogic-settings-passwords-api/) — Password policies allow you to configure various rules for enforcing password strength, for both devices and users. These settings are used in the strength…
- [ScienceLogic Settings/Public Key API](https://apis.io/apis/sciencelogic/sciencelogic-settings-publickey-api/) — Returns the default public keys for your appliance that can be used for public key authentication with devices that support it.
- [ScienceLogic Settings/Security API](https://apis.io/apis/sciencelogic/sciencelogic-settings-security-api/) — Configure various global settings to mandate a higher level of network security for the Skylar Compliance appliance. Setting some of these options may cause…
- [ScienceLogic Settings/Security/CSR API](https://apis.io/apis/sciencelogic/sciencelogic-settings-security-csr-api/) — Manage TLS CSRs
- [ScienceLogic Settings/Security/SSH API](https://apis.io/apis/sciencelogic/sciencelogic-settings-security-ssh-api/) — Manage SSH settings
- [ScienceLogic Settings/Security/TLS API](https://apis.io/apis/sciencelogic/sciencelogic-settings-security-tls-api/) — Configure TLS certificate and key
- [ScienceLogic Settings/SNMP API](https://apis.io/apis/sciencelogic/sciencelogic-settings-snmp-api/) — If your network has a Network Management System, you can use SNMP to perform some basic monitoring of the Skylar Compliance appliance. Skylar Compliance…
- [ScienceLogic Status API](https://apis.io/apis/sciencelogic/sciencelogic-status-api/) — Retrieve status information for the appliance.
- [ScienceLogic Status/Ping API](https://apis.io/apis/sciencelogic/sciencelogic-status-ping-api/) — Check if appliance is ready to accept requests
- [ScienceLogic Syslog API](https://apis.io/apis/sciencelogic/sciencelogic-syslog-api/) — These are the messages logged to the Skylar Compliance syslog service, by both the appliance itself and any devices configured to log to it.
- [ScienceLogic Table view API](https://apis.io/apis/sciencelogic/sciencelogic-table-view-api/) — The Table view API from ScienceLogic — 2 operation(s) for table view.
- [ScienceLogic Template API](https://apis.io/apis/sciencelogic/sciencelogic-template-api/) — Templates are specially marked-up configurations that can be pushed to multiple devices, for instance during a large deployment of similarly configured…
- [ScienceLogic Token API](https://apis.io/apis/sciencelogic/sciencelogic-token-api/) — Personal access tokens are used to authenticate requests to the API. Tokens are tied to the user that created them. All API operations undertaken via a…
- [ScienceLogic Transcript API](https://apis.io/apis/sciencelogic/sciencelogic-transcript-api/) — Device command and backup transcripts can be retrieved here.
- [ScienceLogic User API](https://apis.io/apis/sciencelogic/sciencelogic-user-api/) — Skylar Compliance supports three levels of user access: - **Admin:** Super User; has full control (can create/modify/delete devices and users, initiate…
- [ScienceLogic User/LDAP API](https://apis.io/apis/sciencelogic/sciencelogic-user-ldap-api/) — For LDAP users to be able to login to Skylar Compliance, they need to be a member of a group and the group has to be added to Skylar Compliance (with…
- [ScienceLogic File Server API](https://apis.io/apis/sciencelogic/sciencelogic-file-server-api/) — A file server represents a remote storage location that can be used for archiving Skylar Compliance, exporting backups and automated exports.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Sciencelogic Webhooks](https://apis.io/asyncapis/sciencelogic/sciencelogic-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [ScienceLogic MCP (mcp-sl)](https://apis.io/servers/sciencelogic/sciencelogic-mcp-mcp-sl/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Sciencelogic Agentic Access](https://apis.io/agentic-access/sciencelogic/sciencelogic-agentic-access/)

#### Overlays (2)

OpenAPI overlays, including conversational phrasing for each operation.

- [Sciencelogic Agent Api Overlay](https://apis.io/overlays/sciencelogic/sciencelogic-agent-api-overlay/)
- [Sciencelogic Skylar Compliance Overlay](https://apis.io/overlays/sciencelogic/sciencelogic-skylar-compliance-overlay/)

#### Governance rules (1)

Spectral rulesets for the provider's contracts.

- [ScienceLogic API Rules](https://apis.io/rules/sciencelogic/sciencelogic-rules/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Sciencelogic Authentication](https://apis.io/security/sciencelogic/sciencelogic-authentication/)
- [Sciencelogic Domain Security](https://apis.io/security/sciencelogic/sciencelogic-domain-security/)
- [Sciencelogic Trust Center](https://apis.io/security/sciencelogic/sciencelogic-trust-center/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Sciencelogic Plans Pricing](https://apis.io/plans/sciencelogic/sciencelogic-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Sciencelogic Rate Limits](https://apis.io/rate-limits/sciencelogic/sciencelogic-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Sciencelogic Finops](https://apis.io/finops/sciencelogic/sciencelogic-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://sciencelogic.com)
- [Documentation](https://docs.sciencelogic.com)
- [Getting started](https://docs.sciencelogic.com/latest/Content/Web_Content_Dev_and_Integration/ScienceLogic_API/api_intro.htm)
- [API reference](https://docs.sciencelogic.com/skylar_compliance/api/5-6/api.html)
- [Pricing](https://sciencelogic.com/why-sciencelogic/pricing)
- [Sign up](https://sciencelogic.com/get-free-trial)
- [Support](https://support.sciencelogic.com/s/)
- [Blog](https://sciencelogic.com/feed)
- [Terms of service](https://sciencelogic.com/company/standard-terms-and-conditions-v20260116)
- [Privacy policy](https://sciencelogic.com/company/legal)
- [GitHub](https://github.com/ScienceLogic)

## API Evangelist rating

**Kin Score 58.0** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 63.3 |
| Contract quality | 55.0 |
| Contract governance | 13.6 |
| Operational transparency | 34.2 |
| Developer ergonomics | 54.2 |
| Access clarity | 92.1 |

**Agent readiness 50.6** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | documented (partial credit) |
| Auth Clarity | served (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | verified |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | yes |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | documented (partial credit) |
| Protected Resource Metadata | — |
| Dynamic Client Registration | yes |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | distinct |

**Regulatory alignment 29.4** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/sciencelogic/](https://apis.io/providers/sciencelogic/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for ScienceLogic: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/sciencelogic/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
