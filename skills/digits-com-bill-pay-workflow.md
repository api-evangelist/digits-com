---
name: Run the Digits bill-pay workflow
description: Submit, approve, and pay a bill through the Digits bill workflow, then track its payment status.
api: Digits Connect API
base_url: https://connect.digits.com/v1
operations: [workflowbillservice_submit, workflowbillservice_approve, workflowbillservice_pay, workflowbillservice_updatepaymentstatus, workflowbillservice_query]
scopes: [bills:manage]
---

# Run the Digits bill-pay workflow

Use this skill to move a bill through submission, approval, and payment.

## Auth
- OAuth 2.0 Bearer token with scope `bills:manage`.

## Steps
1. **Submit** — call `workflowbillservice_submit` to submit a bill into the workflow.
2. **Approve** — call `workflowbillservice_approve` to approve the submitted bill (use `workflowbillservice_reject` or `workflowbillservice_void` to decline/cancel).
3. **Pay** — call `workflowbillservice_pay` to schedule/execute payment.
4. **Track** — call `workflowbillservice_updatepaymentstatus` to record payment-status changes, and `workflowbillservice_query` to list bills and their states.

## Rules
- The workflow syncs back to the Agentic General Ledger so payables stay reconciled.
- Rate limits: 60 req/min per token; on 429 back off to `X-RateLimit-Reset`.
- Errors: 403 indicates the token lacks `bills:manage`.
