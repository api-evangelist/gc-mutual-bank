# G&C Mutual Bank (gc-mutual-bank)

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
