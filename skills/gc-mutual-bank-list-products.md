---
name: Retrieve and compare G&C Mutual Bank banking products
description: >-
  Use G&C Mutual Bank's public CDR Product Reference Data API to list banking
  products and fetch full product detail (rates, fees, features, eligibility). No
  authentication is required - this is public Open Banking data.
api: openapi/gc-mutual-bank-cds-banking-products-openapi.yml
operations:
  - listBankingProducts
  - getBankingProductDetail
---

# Retrieve and compare G&C Mutual Bank banking products

This skill covers the **public, unauthenticated** Product Reference Data surface.
Base URL: `https://ibank.gcmutualbank.com.au/openbanking/cds-au/v1`

## Rules (from conventions/ and errors/)
- **Always send the `x-v` header.** Supported versions are `4` and `5`. Omitting it
  returns `400 Header/Missing`; sending `x-v: 3` returns `406 Header/UnsupportedVersion`.
- **No auth.** Do not send tokens or keys; PRD is public.
- **Pagination is 1-based** via `page` and `page-size` (default 25, max 1000). Read
  `meta.totalRecords` and `meta.totalPages`; follow `links.next` until absent.
- **Errors** use the CDS envelope `{ errors: [ { code, title, detail } ] }` with
  `urn:au-cds:error:...` codes - see `errors/gc-mutual-bank-problem-types.yml`.

## Steps

1. **List products** — `listBankingProducts`
   `GET /banking/products` with header `x-v: 4`.
   Optional filters: `product-category`, `brand`, `effective` (CURRENT/FUTURE/ALL),
   `updated-since`, `page`, `page-size`.
   Read `data.products[]` (each has `productId`, `name`, `productCategory`,
   `description`, `brand`). Page through using `links.next` / `meta.totalPages`.

2. **Get product detail** — `getBankingProductDetail`
   `GET /banking/products/{productId}` with header `x-v: 4`, using a `productId`
   returned in step 1. An unknown id returns `404 Resource/NotFound`.
   The response `data` includes `lendingRates`, `depositRates`, `fees`, `features`,
   `constraints`, `eligibility`, and `additionalInformation`.

3. **Compare** — collect the detail objects and compare `depositRates` /
   `lendingRates` / `fees` across products to answer the user's question (e.g.
   best savings rate, lowest home-loan rate, accounts with no monthly fee).
