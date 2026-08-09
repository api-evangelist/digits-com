---
name: Read Digits financial statements
description: Pull profit-and-loss, balance sheet, and cash-flow statements plus AR/AP aging from the Digits ledger.
api: Digits Connect API
base_url: https://connect.digits.com/v1
operations: [companyservice_get, ledgerstatementsservice_profitandloss, ledgerstatementsservice_balancesheet, ledgerstatementsservice_cashflow, ledgerstatementsservice_araging, ledgerstatementsservice_apaging]
scopes: [ledger:read]
---

# Read Digits financial statements

Use this skill to retrieve real-time financial statements from a connected Digits company.

## Auth
- OAuth 2.0 Bearer token with scope `ledger:read`.

## Steps
1. **Identify the company** — call `companyservice_get` to confirm the connected company.
2. **Profit & Loss** — call `ledgerstatementsservice_profitandloss` for the P&L over a period.
3. **Balance sheet** — call `ledgerstatementsservice_balancesheet` for financial position as of a date.
4. **Cash flow** — call `ledgerstatementsservice_cashflow` for the cash-flow statement.
5. **Aging** — call `ledgerstatementsservice_araging` (receivables) and `ledgerstatementsservice_apaging` (payables) for aging schedules.

## Rules
- All statements are generated in real time from the Agentic General Ledger — no export step needed.
- Cursor pagination applies where result sets are large (`limit` + `next.cursor`).
- Rate limits: 60 req/min per token; back off on 429 using `X-RateLimit-Reset`.
