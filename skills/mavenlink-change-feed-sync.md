---
name: mavenlink-change-feed-sync
description: >-
  Keep an external system in sync with Kantata OX using the Subscribed Events change feed instead of polling
  every resource endpoint - including the retention window, the ordering and duplication caveats, and the
  runtime schema lookup that tells you what each event payload contains.
api: Kantata OX API
base_url: https://api.mavenlink.com/api/v1/
generated: '2026-08-25'
method: generated
source: >-
  openapi/mavenlink-openapi.yml + https://developer.kantata.com/kantata/specification/events +
  https://knowledge.kantata.com/hc/en-us/articles/4407962435227-Subscribed-Events-Reference
operations:
  - Get Subscribed Events
  - Get Subscribed Event Types
---

# Sync from Kantata OX with Subscribed Events

Kantata's own documentation tells you to use this instead of polling many endpoints, and it is the documented
mitigation for the 3-minute request timeout.

## What this is not

There are **no webhooks**. Nothing is pushed. There is no subscription resource, no callback URL to register
and no signing secret. You poll.

## Steps

1. **Discover the vocabulary at runtime** - `GET /subscribed_events/event_types.json`
   (`Get Subscribed Event Types`). It returns `subscribed_event_types` (the names) **and**
   `subscribed_event_type_schemas` - a per-event-type map of the documented fields that appear in
   `previous_payload`, `current_payload` and `payload_changes`. Read this rather than hard-coding a field list.
2. **Poll the feed** - `GET /subscribed_events.json` (`Get Subscribed Events`) with:
   - `created_after` / `created_before` - ISO 8601, your watermark
   - `event_types` - comma-separated, e.g. `time_entry:created,time_entry:updated,time_entry:deleted`
   - `include=subject` - adds `subject_ref` (`{id, key}`) so you can resolve what the event is about
   - `most_recent` or `most_recent_by_event_type` - collapse a noisy subject to its latest state. The two are
     mutually exclusive.
3. **Resolve** - use `subject_ref.key` to pick the right resource endpoint and `subject_ref.id` to fetch it.
   `subject_ref` is `null` when the subject was deleted or transferred to another account.

## The three constraints that decide your design

- **Retention is 9 days.** Poll on a cadence comfortably shorter than that. If your consumer is down for nine
  days you have lost the changes and must fall back to a full reconciliation. An Extended History add-on exists
  in beta for Enterprise and Premier accounts.
- **Ordering is not guaranteed.** One user action can emit several events out of order, and `subject_changed_at`
  can differ from `created_at` because of generation lag. Never treat feed order as causal order - reconcile by
  subject, using `subject_changed_at`.
- **Duplicates happen.** The documentation says so explicitly. Deduplicate by event id.

## Access

Subscribed Events is an **add-on**, and only **Account Administrators** can read it. A token belonging to a
non-admin user will 403 - that is an entitlement and permission answer, not a scope answer.

## Coverage

182 event types across 49 subjects, covering workspaces, stories, time entries, timesheets, expenses, expense
budgets, invoices, billing milestones, users, account memberships, access groups and their per-area permission
changes, roles, skills, rate-related objects, organizations, workweeks and custom field values. The full list
is in `asyncapi/mavenlink-event-surface.yml`.
