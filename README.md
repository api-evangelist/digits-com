# Digits

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

**Areas:** Accounting · Bookkeeping · Finance · General Ledger · Artificial Intelligence · Fintech

## Digits on APIs.io

Everything profiled for Digits is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/digits-com/](https://apis.io/providers/digits-com/)** — or go straight to one of the APIs or properties below.

### APIs (12)

- [Digits MCP Server](https://apis.io/apis/digits-com/digits-com-mcp-server/) — Model Context Protocol server that lets AI clients like ChatGPT and Claude connect directly to Digits to query the ledger in natural language. Discovery is…
- [Digits Chart of Accounts API](https://apis.io/apis/digits-com/digits-com-chart-of-accounts-api/) — Ledger categories and dimensional axes (departments, locations, projects).
- [Digits Connections API](https://apis.io/apis/digits-com/digits-com-connections-api/) — Connected data sources feeding the ledger.
- [Digits Financial Statements API](https://apis.io/apis/digits-com/digits-com-financial-statements-api/) — Balance Sheet, P&L, Cash Flow, Trial Balance, aging reports, and summaries.
- [Digits Organizations API](https://apis.io/apis/digits-com/digits-com-organizations-api/) — Accounting-firm organizations, clients, entities, and employees.
- [Digits Parties API](https://apis.io/apis/digits-com/digits-com-parties-api/) — Vendors, suppliers, customers, and other business relationships.
- [Digits Sources API](https://apis.io/apis/digits-com/digits-com-sources-api/) — Push raw source data into the AGL for enrichment and categorization.
- [Digits Transactions API](https://apis.io/apis/digits-com/digits-com-transactions-api/) — Read AI-categorized ledger transactions and journal entries.
- [Digits Webhooks API](https://apis.io/apis/digits-com/digits-com-webhooks-api/) — Receive event notifications from Digits at a configured webhook endpoint; Digits POSTs a JSON event body and expects a 2xx acknowledgment…
- [Digits Llms.txt API](https://apis.io/apis/digits-com/digits-com-llms-txt-api/) — The Llms.txt API from Digits — 1 operation(s) for llms.txt.
- [Digits Sitemap.xml API](https://apis.io/apis/digits-com/digits-com-sitemap-xml-api/) — The Sitemap.xml API from Digits — 1 operation(s) for sitemap.xml.
- [Digits .well Known API](https://apis.io/apis/digits-com/digits-com-well-known-api/) — The .well Known API from Digits — 2 operation(s) for .well known.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Digits Com Webhooks](https://apis.io/asyncapis/digits-com/digits-com-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [Digits MCP](https://apis.io/servers/digits-com/digits-mcp/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Digits Com Agentic Access](https://apis.io/agentic-access/digits-com/digits-com-agentic-access/)

#### Collections (12)

Postman and Open Collection request collections.

- [Digits Connect API](https://apis.io/collections/digits-com/open-digits-com/)
- [Digits Connect Chart of Accounts API](https://apis.io/collections/digits-com/open-digits-com-chart-of-accounts-api/)
- [Digits Connect Chart of Accounts Connections API](https://apis.io/collections/digits-com/open-digits-com-connections-api/)
- [Digits Connect Chart of Accounts Financial Statements API](https://apis.io/collections/digits-com/open-digits-com-financial-statements-api/)
- [Digits Llms.txt API](https://apis.io/collections/digits-com/open-digits-com-llms-txt-api/)
- [Digits Connect Chart of Accounts Organizations API](https://apis.io/collections/digits-com/open-digits-com-organizations-api/)
- [Digits Connect Chart of Accounts Parties API](https://apis.io/collections/digits-com/open-digits-com-parties-api/)
- [Digits Llms.txt Sitemap.xml API](https://apis.io/collections/digits-com/open-digits-com-sitemap-xml-api/)
- [Digits Connect Chart of Accounts Sources API](https://apis.io/collections/digits-com/open-digits-com-sources-api/)
- [Digits Connect Chart of Accounts Transactions API](https://apis.io/collections/digits-com/open-digits-com-transactions-api/)
- [Digits Connect Chart of Accounts Webhooks API](https://apis.io/collections/digits-com/open-digits-com-webhooks-api/)
- [Digits Llms.txt .well Known API](https://apis.io/collections/digits-com/open-digits-com-well-known-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Digits Com Overlay](https://apis.io/overlays/digits-com/digits-com-overlay/)

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Digits Com Authentication](https://apis.io/security/digits-com/digits-com-authentication/)
- [Digits Com Domain Security](https://apis.io/security/digits-com/digits-com-domain-security/)
- [Digits Com Trust Center](https://apis.io/security/digits-com/digits-com-trust-center/)
- [Digits Com Vulnerability Disclosure](https://apis.io/security/digits-com/digits-com-vulnerability-disclosure/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Digits Com Scopes](https://apis.io/scopes/digits-com/digits-com-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Digits Com Plans Pricing](https://apis.io/plans/digits-com/digits-com-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Digits Com Rate Limits](https://apis.io/rate-limits/digits-com/digits-com-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Digits Com Finops](https://apis.io/finops/digits-com/digits-com-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://digits.com)
- [Documentation](https://developer.digits.com)
- [Getting started](https://developer.digits.com/docs/app-creation)
- [API reference](https://developer.digits.com/reference/companyservice_get)
- [Pricing](https://digits.com/pricing)
- [Sign up](https://my.digits.com)
- [Support](https://help.digits.com)
- [Blog](https://digits.com/blog/rss.xml)
- [Security](https://digits.com/security/)
- [Compliance](https://trust.digits.com)
- [Terms of service](https://my.digits.com/legal/terms-of-service)
- [Privacy policy](https://my.digits.com/legal/privacy-policy)
- [GitHub](https://github.com/digits)

## API Evangelist rating

**Kin Score 52.5** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 64.3 |
| Contract quality | 52.9 |
| Contract governance | 18.2 |
| Operational transparency | 34.2 |
| Developer ergonomics | 48.2 |
| Access clarity | 57.9 |

**Agent readiness 35.7** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | negotiable (partial credit) |
| Idempotency | documented (partial credit) |
| Error Semantics | documented (partial credit) |
| OpenAPI Examples | — |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | yes |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | documented (partial credit) |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | distinct |

**Regulatory alignment 34.5** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/digits-com/](https://apis.io/providers/digits-com/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Digits: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/digits-com/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
