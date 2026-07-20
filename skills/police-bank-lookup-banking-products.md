---
name: Look up Police Bank banking products (CDR PRD)
description: Discover Police Bank's publicly available banking products and retrieve full product detail (rates, fees, features, eligibility) via the unauthenticated Consumer Data Right Product Reference Data API.
api: openapi/police-bank-cds-banking-products-openapi.yml
operations: [listBankingProducts, getBankingProductDetail]
auth: none
base_url: https://public.cdr.prd.policebank.com.au/cds-au/v1
---

# Look up Police Bank banking products

Police Bank publishes a public, **unauthenticated** Consumer Data Right (CDR)
Product Reference Data (PRD) API. Use it to enumerate products and read their
full terms. No API key or token is required.

## Rules
- Send a mandatory `x-v` header on every request (integer endpoint version).
  Optionally send `x-min-v` to accept an older version if the requested one is
  unsupported.
- Base URL: `https://public.cdr.prd.policebank.com.au/cds-au/v1`.
- Read-only: there are no state-changing operations, so idempotency keys are not
  used. Safe to retry on network failure.
- Errors come back as the CDS envelope `{ "errors": [ { "code", "title",
  "detail" } ] }`. Common codes: `Header/UnsupportedVersion` (406),
  `Field/InvalidPageSize` (400), `Field/InvalidPage` (422),
  `Resource/Unavailable` / `Resource/Invalid` (404). See
  `errors/police-bank-problem-types.yml`.

## Steps

1. **List products** — `listBankingProducts`
   `GET /banking/products` with header `x-v: 3`.
   Optional filters: `product-category`, `brand`, `effective`
   (CURRENT|FUTURE|ALL), `updated-since`. Paginate with `page` / `page-size`;
   read `meta.totalPages` / `meta.totalRecords` and follow `links.next`.

2. **Get product detail** — `getBankingProductDetail`
   Take a `productId` from step 1 and call
   `GET /banking/products/{productId}` with header `x-v: 7`.
   The response includes `fees`, `depositRates`, `lendingRates`, `features`,
   `constraints`, `eligibility`, and `bundles`
   (see `data-model/police-bank-data-model.yml`).

3. **Handle version negotiation** — if you receive `406 Unsupported Version`,
   retry with a different `x-v` (or set `x-min-v`) per
   `lifecycle/police-bank-lifecycle.yml`.
