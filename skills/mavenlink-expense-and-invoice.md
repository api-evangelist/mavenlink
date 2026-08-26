---
name: mavenlink-expense-and-invoice
description: >-
  Record expenses against a Kantata OX project budget, run them through the expense-report approval flow, and
  generate and cancel client invoices - including the cancel-versus-delete distinction that decides whether the
  financial record survives.
api: Kantata OX API
base_url: https://api.mavenlink.com/api/v1/
generated: '2026-08-25'
method: generated
source: openapi/mavenlink-openapi.yml + https://developer.kantata.com/
operations:
  - Get Expense Categories
  - Create Expense
  - Update Expense
  - Delete Expense
  - Create Expense Budget
  - Create Expense Report Submission
  - Approve Expense Report Submission
  - Reject Expense Report Submission
  - Cancel Expense Report Submission
  - Get Next Invoice Number
  - Create Invoice
  - Update Invoice
  - Cancel Invoice
  - Delete Invoice
  - Update Workspace Expense Approval Setting
---

# Expenses and invoicing in Kantata OX

## Expenses

1. `GET /expense_categories.json` (`Get Expense Categories`) - categories are account-level; do not invent one.
2. `POST /expenses.json` (`Create Expense`) against a `workspace_id`, `expense_category_id`, `user_id` and
   optionally `story_id`, `vendor_id` and `expense_budget_id`.
3. `POST /expense_report_submissions.json` (`Create Expense Report Submission`) to send them for approval.
4. `PUT /expense_report_submissions/{id}/approve.json` (`Approve Expense Report Submission`).

**Reversal:** `Cancel Expense Report Submission` (`PUT /expense_report_submissions/{id}/cancel.json`) unwinds a
submission; `Reject Expense Report Submission` unwinds an approval decision. Neither has a stated time window.
`Delete Expense` and the bulk `DELETE /expenses.json` are irreversible.

## Invoices

1. `GET /invoices/next_invoice_number.json` (`Get Next Invoice Number`) - **call this first.** Do not generate
   an invoice number yourself; the account owns the sequence.
2. `POST /invoices.json` (`Create Invoice`). An invoice draws together `time_entry_ids`, `expense_ids`,
   `billing_milestone_ids`, `fixed_fee_item_ids` and `additional_item_ids` across one or more `workspace_ids`.
3. `PUT /invoices/{id}.json` (`Update Invoice`) while it is still editable.

**Cancel is not delete, and the difference is the whole point:**

- `Cancel Invoice` - `PUT /invoices/{id}/cancel.json` - voids the invoice and **keeps the record**, which is
  what an accounting audit trail needs. This is the reversal an agent should reach for.
- `Delete Invoice` - `DELETE /invoices/{id}.json` - removes it. There is no restore. Do not call this to
  "undo" an invoice; call cancel.

## Retries and duplicates

No idempotency key exists on this API. A retried `Create Invoice` after a 3-minute timeout can produce a second
invoice consuming the same time entries. Always `GET /invoices.json` filtered to the workspace and check before
retrying, and remember that `Get Next Invoice Number` will have advanced.

## Errors

`422` returns `errors[].field` naming the offending attribute. `403` means the user's access group lacks
financial-management permission - it is not a token-scope problem and re-authorising will not fix it.
