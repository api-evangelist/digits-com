# Digits (digits-com)

Digits is an AI-native accounting and bookkeeping platform for startups and their accountants, built around the Autonomous General Ledger (AGL) that auto-books the majority of transactions in real time. The Digits Connect API opens the AGL programmatically over REST with OAuth 2.0, letting partners send raw transaction, party, and dimension data for AI categorization and vendor enrichment, and read back ledger entries and financial statements. Digits also publishes an MCP server for AI agents (ChatGPT, Claude) to query the ledger.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/digits-com/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/digits-com/refs/heads/main/apis.yml)

## API Availability

Digits is primarily an AI accounting/bookkeeping product, but it **does expose a real, documented public first-party API** — the **Digits Connect API**, launched in late 2025. It is free (no partner fees, usage paywalls, or marketplace lock-ins), uses OAuth 2.0 (authorization code grant), has a live developer portal at [developer.digits.com](https://developer.digits.com), cursor-based pagination, idempotent source-sync endpoints (via `external_id`), webhooks, and a published MCP server. The Connect API base URL is `https://connect.digits.com/v1`.

Note: `https://digits.com/openapi.json` exists but describes only marketing-site / MCP-discovery metadata (llms.txt, sitemap, `.well-known/mcp`), **not** the Connect API. See [review.yml](review.yml) for the full availability finding.

## Tags

- Accounting
- Bookkeeping
- Finance
- General Ledger
- AI
- FinTech

## Timestamps

- **Created:** 2026-07-01
- **Modified:** 2026-07-01

## APIs

### Digits Transactions API

Read AI-categorized ledger transactions and journal entries, query entries by filter, and retrieve individual transactions from the Autonomous General Ledger.

- **Human URL:** [https://developer.digits.com](https://developer.digits.com)
- **Base URL:** `https://connect.digits.com/v1`

#### Tags

- Transactions
- Ledger
- Journal Entries

#### Properties

- [Documentation](https://developer.digits.com)
- [OpenAPI](openapi/digits-com-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/digits-com.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/digits-com.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Digits Source Sync API

Push raw source data — transactions, parties, products, departments, locations, and projects — into the AGL for AI research, enrichment, and categorization. Idempotence and deduplication are handled via the `external_id` field.

- **Human URL:** [https://developer.digits.com](https://developer.digits.com)
- **Base URL:** `https://connect.digits.com/v1`

#### Tags

- Ingestion
- Sync
- Idempotency

#### Properties

- [Documentation](https://developer.digits.com)
- [OpenAPI](openapi/digits-com-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/digits-com.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)

### Digits Parties API

List and retrieve parties — the vendors, suppliers, customers, and other business relationships that Digits hydrates and enriches from transaction data.

- **Human URL:** [https://developer.digits.com](https://developer.digits.com)
- **Base URL:** `https://connect.digits.com/v1`

#### Tags

- Parties
- Vendors
- Customers

#### Properties

- [Documentation](https://developer.digits.com)
- [OpenAPI](openapi/digits-com-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Digits Chart of Accounts API

List and retrieve ledger categories (chart of accounts) plus the dimensional accounting axes — departments, locations, and projects — used to classify financial data.

- **Human URL:** [https://developer.digits.com](https://developer.digits.com)
- **Base URL:** `https://connect.digits.com/v1`

#### Tags

- Chart of Accounts
- Categories
- Dimensions

#### Properties

- [Documentation](https://developer.digits.com)
- [OpenAPI](openapi/digits-com-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Digits Financial Statements API

Generate core financial statements directly from the ledger — Balance Sheet, Profit and Loss, Cash Flow, Trial Balance, A/P Aging, and A/R Aging — plus ledger summaries.

- **Human URL:** [https://developer.digits.com](https://developer.digits.com)
- **Base URL:** `https://connect.digits.com/v1`

#### Tags

- Reports
- Financial Statements
- Balance Sheet

#### Properties

- [Documentation](https://developer.digits.com)
- [OpenAPI](openapi/digits-com-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Digits Connections API

List and sync the connected data sources feeding the ledger, covering the 12,000+ financial-institution and payments integrations Digits ingests from.

- **Human URL:** [https://developer.digits.com](https://developer.digits.com)
- **Base URL:** `https://connect.digits.com/v1`

#### Tags

- Connections
- Data Sources
- Integrations

#### Properties

- [Documentation](https://developer.digits.com)
- [OpenAPI](openapi/digits-com-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Digits Organizations API

Manage accounting-firm organizations and their client books, entities, and employees, including bulk operations for onboarding clients at scale.

- **Human URL:** [https://developer.digits.com](https://developer.digits.com)
- **Base URL:** `https://connect.digits.com/v1`

#### Tags

- Organizations
- Clients
- Firms

#### Properties

- [Documentation](https://developer.digits.com)
- [OpenAPI](openapi/digits-com-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Digits Webhooks API

Receive event notifications from Digits at a configured webhook endpoint; Digits POSTs a JSON event body and expects a 2xx acknowledgment.

- **Human URL:** [https://developer.digits.com](https://developer.digits.com)
- **Base URL:** `https://connect.digits.com/v1`

#### Tags

- Webhooks
- Events
- Notifications

#### Properties

- [Documentation](https://developer.digits.com)

### Digits MCP Server

Model Context Protocol server that lets AI clients like ChatGPT and Claude connect directly to Digits to query the ledger in natural language. Discovery is published as an MCP Server Card at `/.well-known/mcp/server.json`.

- **Human URL:** [https://developer.digits.com](https://developer.digits.com)
- **Base URL:** `https://digits.com`

#### Tags

- MCP
- AI Agents
- Model Context Protocol

#### Properties

- [Documentation](https://developer.digits.com)
- [MCP](https://digits.com/.well-known/mcp/server.json) — [Model Context Protocol](https://modelcontextprotocol.io)

## Common Properties

- [GitHub Organization](https://github.com/digits)
- [LinkedIn](https://www.linkedin.com/company/digits-financial)
- [Website](https://digits.com)
- [Documentation](https://developer.digits.com)
- [Plans](plans/digits-com-plans-pricing.yml)
- [Rate Limits](rate-limits/digits-com-rate-limits.yml)
- [Fin Ops](finops/digits-com-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
