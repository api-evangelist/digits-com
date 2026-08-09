---
name: Sync source transactions into Digits
description: Create/update a Digits source and idempotently sync financial transactions into it, then read them back from the ledger.
api: Digits Connect API
base_url: https://connect.digits.com/v1
operations: [connectionsourceservice_sync, sourcepartyservice_sync, sourcetransactionservice_sync, ledgertransactionservice_queryentries]
scopes: [source:sync, ledger:read]
---

# Sync source transactions into Digits

Use this skill to write financial transactions from an external system into Digits and confirm they landed in the ledger.

## Auth
- OAuth 2.0 authorization-code grant. Send `Authorization: Bearer <access_token>`.
- Requires scopes `source:sync` (writes) and `ledger:read` (read-back).

## Steps
1. **Create/refresh the source** — call `connectionsourceservice_sync` to create the dedicated source that will organize your transactions. Sources are isolated bankfeeds with their own `externalId` key space.
2. **(Optional) Sync parties** — call `sourcepartyservice_sync` to create counterparties referenced by transactions.
3. **Sync transactions** — call `sourcetransactionservice_sync` with your transaction records. Writes are **idempotent on `externalId`**: re-sending the same `externalId` upserts (updates) the record instead of duplicating it. `externalId` is scoped to the source.
4. **Read back** — call `ledgertransactionservice_queryentries` (scope `ledger:read`) to confirm Digits processed, categorized, and matched the transactions into the ledger.

## Rules
- Idempotency: always set a stable `externalId` per transaction; the most recent write wins.
- Pagination: list/query endpoints are cursor-based — pass `limit`, follow `next.cursor` while `next.more` is true.
- Rate limits: 60 req/min per access token, 180 req/min per client. On HTTP 429 back off to `X-RateLimit-Reset`.
- Errors: 401 (bad/expired token), 403 (missing scope), 429 (rate limited).
