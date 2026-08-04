# UK Open Banking

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

UK Open Banking standard with REST APIs for account and transaction data, payment initiation, variable recurring payments, and confirmation of funds for regulated financial services. Governed by the Open Banking Implementation Entity (OBIE) and overseen by the FCA and PSR under PSD2 and the CMA Order.

## APIs

### Read/Write API v4.0.1
The core Open Banking API enabling TPPs to access customer account information and initiate payments with consent. Covers four service roles:

- **AISP (Account Information Service Provider)** — Account access consents, accounts, balances, transactions, beneficiaries, direct debits, standing orders, products, offers, parties, scheduled payments, and statements
- **PISP (Payment Initiation Service Provider)** — Domestic and international immediate payments, scheduled payments, and standing orders
- **CBPII (Card-Based Payment Instrument Issuer)** — Confirmation of funds (CoF) to verify available balances before payment
- **VRP (Variable Recurring Payments)** — Domestic VRP consents and payment orders for flexible, customer-controlled recurring payments

Documentation: https://openbankinguk.github.io/read-write-api-site3/v4.0.1/

### Open Data API v2.4.0
Public APIs requiring no customer authentication for accessing standardized bank product and location data:
- ATM locations
- Branch locations
- Personal current account products
- Business current account products
- SME commercial credit cards
- SME loans

Documentation: https://openbankinguk.github.io/opendata-api-docs-pub/

### Dynamic Client Registration API v3.3
Enables TPPs to register dynamically as OAuth clients with ASPSPs by submitting Software Statement Assertions from the Open Banking Directory.

### Directory API
Manages participant registration, Software Statement management, and service discovery for the UK Open Banking ecosystem.

## Access Model

Core mandated APIs are available free of charge to FCA-authorised TPPs registered on the Open Banking Directory. Premium APIs (e.g., commercial VRP) are subject to bilateral commercial agreements governed by JROC pricing principles.

- Standards: https://standards.openbanking.org.uk/
- Developer Zone: https://openbanking.atlassian.net/wiki/spaces/DZ/overview
- GitHub: https://github.com/OpenBankingUK
- API Performance: https://www.openbanking.org.uk/api-performance/

## Performance Standards

- Availability target: 99.5% monthly
- Response time target: 750ms average TTLB (AISP, PISP, CoF)
- Error rate target: 0.5% maximum daily error rate (5xx responses)

## Repository Structure

- `apis.yml` — APIs.json 0.19 provider profile
- `plans/plans.yml` — API access plans and tiers
- `rate-limits/rate-limits.yml` — Performance KPIs and rate limit guidance
- `finops/finops.yml` — FinOps considerations for API consumers
