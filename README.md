# UK Open Banking

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
