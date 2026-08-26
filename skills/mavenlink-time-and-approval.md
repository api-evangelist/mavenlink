---
name: mavenlink-time-and-approval
description: >-
  Log time against Kantata OX tasks, submit a timesheet for approval, and approve, reject or cancel
  submissions - individually or in bulk - with the reversal path for each write.
api: Kantata OX API
base_url: https://api.mavenlink.com/api/v1/
generated: '2026-08-25'
method: generated
source: openapi/mavenlink-openapi.yml + https://developer.kantata.com/
operations:
  - Get Time Entries
  - Create Time Entry
  - Update Time Entry
  - Delete Time Entry
  - Create Timesheet Submission
  - Get Timesheet Submissions
  - Approve Timesheet Submission
  - Reject Timesheet Submission
  - Cancel Timesheet Submission
  - Approve Timesheet Submissions
  - Reject Timesheet Submissions
  - Cancel Timesheet Submissions
  - Update Workspace Time Approval Setting
---

# Log and approve time in Kantata OX

## Steps

1. **Check approvals are on for the project** - `PUT /workspaces/{id}/toggle_time_approvals.json`
   (`Update Workspace Time Approval Setting`) controls whether submissions are required at all. Read the
   workspace first rather than toggling blind; this changes behaviour for every person on the project.
2. **Log time** - `POST /time_entries.json` (`Create Time Entry`). A time entry belongs to a `workspace_id`,
   a `user_id`, optionally a `story_id` (task) and a `role_id`.
3. **Correct before submitting** - `PUT /time_entries/{id}.json` (`Update Time Entry`). Once a time entry is
   attached to an active submission it carries `active_submission_id`; check that before editing.
4. **Submit** - `POST /timesheet_submissions.json` (`Create Timesheet Submission`).
5. **Approve** - `PUT /timesheet_submissions/{id}/approve.json` (`Approve Timesheet Submission`), or in bulk
   with `POST /timesheet_approvals.json` (`Approve Timesheet Submissions`).

## Reversing each step

This is the part to read **before** acting, not after.

| Forward action | Reversal | Window |
|---|---|---|
| `Create Timesheet Submission` | `Cancel Timesheet Submission` (`PUT /timesheet_submissions/{id}/cancel.json`) | Gated on submission state, not elapsed time. Not stated in the docs. |
| bulk submit | `Cancel Timesheet Submissions` (`POST /timesheet_cancellations.json`) | as above |
| `Approve Timesheet Submission` | `Reject Timesheet Submission` (`PUT /timesheet_submissions/{id}/reject.json`) | not stated |
| bulk approve | `Reject Timesheet Submissions` (`POST /timesheet_rejections.json`) | as above |
| `Create Time Entry` | `Delete Time Entry` (`DELETE /time_entries/{id}.json`) | **Irreversible.** No restore endpoint. |

`DELETE /time_entries.json` deletes **multiple** entries in one call. Treat it as the highest-consequence
operation in this skill and never call it without an explicit, enumerated id list you have just read back.

## Retries

There is no idempotency key. `Create Time Entry` retried after a timeout produces a duplicate entry that then
flows into a submission and an invoice. Before retrying, `GET /time_entries.json` filtered to the user, the
workspace and the date and confirm what actually landed.

## Watching what changed

The Subscribed Events feed carries `time_entry:created`, `time_entry:updated`, `time_entry:deleted`,
`timesheet:created`, `timesheet:updated` and `timesheet:time_entry_added`. Retention is **9 days**, ordering
is not guaranteed and duplicates are possible - deduplicate by event id and reconcile by subject.
