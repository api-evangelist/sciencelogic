---
name: sciencelogic-backup-diff-and-restore
description: Investigate what changed in a network device's configuration using ScienceLogic Skylar Compliance backups, and — only on explicit human approval — restore a known-good backup.
api: Skylar Compliance API 2.0
base_url: https://{appliance}/api/v2
operations:
  - list_devices
  - get_device
  - list_device_backups
  - get_backup
  - config_details
  - diff_backup
  - restore_backup
  - list_jobs
  - get_job
  - cancel_job
generated: '2026-08-29'
method: generated
source: openapi/sciencelogic-skylar-compliance-openapi.json
---

# Diff and restore a device configuration

This skill has a **write** step. Steps 1–5 are read-only investigation. Step 6 changes a production
network device and must not run without explicit human approval in the same conversation.

## Before you start

- Base URL: `https://{appliance}/api/v2` on the customer's own appliance.
- Auth: `Authorization: Custom <token>`.
- Permissions: reads need `ViewDevices`, `ListBackups`, `ViewBackup`. The restore step needs
  `RestoreDevice` — a different permission, deliberately.

## Steps

1. **Find the device.** `GET /devices` (`list_devices`) with a `search` term, then `GET /devices/{id}`
   (`get_device`) to confirm you have the right one. Read back the device name to the human before going
   further.

2. **List its backups.** `GET /devices/{id}/backups` (`list_device_backups`). Sort newest first with
   `sort=-Date`. Note `LastSuccessfulBackupID` on the device record — that is the most recent good
   configuration and usually the restore target.

3. **Read a backup's metadata.** `GET /devices/{id}/backups/{backup_id}` (`get_backup`).

4. **Read the configuration itself.** `POST /devices/{id}/backups/{backup_id}/config`
   (`config_details`) returns the lines of the backup. Use `byte_offset` for large configs.

5. **Diff two backups.** `POST /devices/backups/diff` (`diff_backup`) with the two backup ids. Present
   the diff to the human. In almost every incident this is where the answer is, and the skill should stop
   here.

6. **Restore — approval gate.** `POST /devices/{id}/backups/{backup_id}/restore` (`restore_backup`).
   Before calling it you MUST:
   - state the device name, the backup id and the backup's date;
   - state that this pushes configuration to a live network device;
   - get an explicit yes.

   The API has **no idempotency keys and no dry-run mode**. Do not "retry" a restore that timed out —
   go to step 7 and find the job instead.

## Step 7 — track the job

Restores are asynchronous. The call returns a job; then:

- `GET /jobs` (`list_jobs`) — running jobs. `GET /jobs/{id}` (`get_job`) — one job.
- `GET /jobs/historic` (`list_historic_jobs`) — completed jobs.
- `DELETE /jobs/{id}` (`cancel_job`) — cancel, but only while the job is still running.

## Reversibility

- A restore is reversible **only if another backup still exists** to restore back to. Retention is set per
  appliance (`GET /settings/archive`, `RetentionDays`/`RetentionPolicy`); there is no vendor-guaranteed
  window. Read the retention setting before you promise a rollback is possible.
- `DELETE /devices/{id}/backups/{backup_id}` destroys the artifact a rollback would need, and has no undo.
  Never call it in this workflow.
