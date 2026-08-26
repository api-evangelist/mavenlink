---
name: mavenlink-project-setup
description: >-
  Stand up a new client project in Kantata OX (formerly Mavenlink) end to end - create the workspace, apply a
  project template, invite participants, assign resources and set the invoice preferences - using only
  operations that exist in the published Kantata OX contract.
api: Kantata OX API
base_url: https://api.mavenlink.com/api/v1/
generated: '2026-08-25'
method: generated
source: openapi/mavenlink-openapi.yml + https://developer.kantata.com/
operations:
  - Create Workspace
  - Apply Project Template To Workspace
  - Create Workspace Invitation
  - Create Participation
  - Create Workspace Resource
  - Create Workspace Allocation
  - Create Workspace Invoice Preferences
  - Get Workspace
  - Update Workspace
  - Delete Workspace
---

# Set up a Kantata OX project

A project is called a **workspace** everywhere in this API. Tasks are called **stories**.

## Before you start

- Send `Authorization: Bearer <token>` on every request. The published spec declares its security schemes but
  never applies them, so a generated client will omit this header - add it yourself.
- Two of the operations in this skill (`Create Workspace` and `Create Workspace Invitation`) carry their own
  rate limits **on top of** the general limit. The numbers are not public. Space these calls out.
- **There is no idempotency key on this API.** If `Create Workspace` times out (requests time out at 3 minutes)
  you do not know whether the workspace was created. Do not blind-retry: call `Get Workspaces` with a `search`
  or `order=created_at:desc` filter and check before retrying.

## Steps

1. **Create the workspace** - `POST /workspaces.json` (`Create Workspace`). A title is required; the 422
   response will name the missing field in `errors[].field` (`"Please give your project a title"` on `title`,
   `"Please select a role for this project"` on `creator_role`).
2. **Apply a template if you have one** - `PUT /workspaces/{id}/apply_template.json`
   (`Apply Project Template To Workspace`). Read the available templates first with `Get Project Templates`.
3. **Invite the client** - `POST /workspaces/{id}/invite.json` (`Create Workspace Invitation`). Rate limited.
4. **Add internal participants** - `POST /participations.json` (`Create Participation`) for each user, or
   `POST /workspace_resources.json` (`Create Workspace Resource`) when you are staffing a named or unnamed role
   rather than adding a collaborator.
5. **Allocate time** - `POST /workspace_allocations.json` (`Create Workspace Allocation`). If you already have
   scheduled hours, `POST /workspace_resources/{id}/allocations_matching_scheduled_hours.json` derives the
   allocation for you.
6. **Set billing behaviour** - `POST /workspace_invoice_preferences.json`
   (`Create Workspace Invoice Preferences`).
7. **Verify** - `GET /workspaces/{id}.json` with `include=participations,workspace_resources` and read the
   `results` array, not the top-level collections.

## Reading the response

Every GET returns `count`, a `results` array of `{key, id}` references **in sorted order**, and one id-keyed
top-level object per collection. Always iterate `results` - reading `workspaces` directly mixes your matches
with side-loaded associations of the same type.

## If something goes wrong

| Status | Meaning | What to do |
|---|---|---|
| 401 | `{"errors":[{"type":"oauth",...}]}` | Token missing, invalid or revoked. Re-run the authorization-code flow. |
| 403 | Permitted user, forbidden action | Kantata authorises through access groups and project participation, not OAuth scopes. Changing scopes will not fix it. |
| 404 on a show route | May be a **default filter**, not a missing record | Read the endpoint's filter defaults and disable the one excluding it. `GET /workspaces.json?only={id}` does not apply the same behaviour. |
| 422 | Validation | Map each `errors[].field` back to the attribute you sent. |
| 429 | Rate limited | Retry after a short delay. No `Retry-After` or `RateLimit-*` header is returned. |

## Undoing this

`DELETE /workspaces/{id}.json` (`Delete Workspace`) is a **hard delete**. There is no restore, undelete or
trash endpoint anywhere in this API and no published grace period. Archiving is the reversible alternative -
see `Unarchive Workspace With Approvals` (`PUT /workspaces/{id}/unarchive_with_approvals.json`) for the
inverse. Do not delete a workspace on an agent's own initiative.
