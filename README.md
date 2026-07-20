# G&C Mutual Bank (gc-mutual-bank)

G&C Mutual Bank is an Australian customer-owned mutual bank and authorised deposit-taking institution (ADI) providing retail and business banking to its members, including home loans, transaction and savings accounts, and credit cards. It merged with Unity Bank effective 7 March 2025, with the combined entity renamed Unity Bank Limited from 1 July 2025; the G&C Mutual Bank brand and its digital banking host remain operational during the multi-brand consolidation, while the public website gcmutual.bank now redirects to unity.bank. Under Australia's Consumer Data Right (CDR / Open Banking) the bank exposes a public, unauthenticated Product Reference Data (PRD) API conforming to the Data Standards Body (DSB) Consumer Data Standards.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/gc-mutual-bank/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/gc-mutual-bank/refs/heads/main/apis.yml)

## Tags

- Financial
- Banks
- Open Banking
- CDR
- Consumer Data Right
- Consumer Banking
- Mutual Bank
- Australia

## Timestamps

- **Created:** 2026-07-20
- **Modified:** 2026-07-20

## APIs

### G&C Mutual Bank CDR Product Reference Data API

Public, unauthenticated Consumer Data Right Product Reference Data (PRD) API exposing G&C Mutual Bank's banking products - eligibility, features, pricing, rates, and links to terms - via `GET /banking/products` and `GET /banking/products/{productId}` under the standard CDS path `/cds-au/v1/banking/products`. Confirmed live returning HTTP 200 with 25 products at supported header version `x-v 4` (`x-v` 4 and 5 available). The contract is the shared DSB Consumer Data Standards CDR Banking API, not a bank-proprietary specification.

- **Human URL:** [https://unity.bank/about-us/corporate-information/open-banking/](https://unity.bank/about-us/corporate-information/open-banking/)
- **Base URL:** `https://ibank.gcmutualbank.com.au/openbanking/cds-au/v1`

#### Tags

- CDR
- Open Banking
- Product Reference Data
- Banking Products
- Public API

#### Properties

- [Documentation](https://unity.bank/about-us/corporate-information/open-banking/)
- [API Reference](https://consumerdatastandardsaustralia.github.io/standards/#cdr-banking-api_get-products)
- [OpenAPI](openapi/gc-mutual-bank-cds-banking-products-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html) (shared DSB Consumer Data Standards CDR Banking API, v1.36.0 — not bank-proprietary)

## Common Properties

- [Website](https://unity.bank/)
- [Documentation](https://unity.bank/about-us/corporate-information/open-banking/)
- [Privacy Policy](https://unity.bank/about-us/privacy/)
- [Support](https://unity.bank/talk-to-us/contact-us/)
- [Blog](https://unity.bank/latest-news/)
- [LinkedIn](https://www.linkedin.com/company/unity-bank)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
