# Digits (digits-com)

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
