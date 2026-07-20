# Police Bank (police-bank)

Police Bank is a mutual, member-owned Australian bank (ABN 95 087 650 799, AFSL / Australian Credit Licence No. 240018) founded to serve the New South Wales police community and their families, now open to the wider public. As an Authorised Deposit-taking Institution it participates in Australia's Consumer Data Right (Open Banking) regime as an active data holder — publishing an unauthenticated Product Reference Data (PRD) API that conforms to the Consumer Data Standards, and letting members share their banking data with ACCC-accredited data recipients.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/police-bank/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/police-bank/refs/heads/main/apis.yml)

## Tags

- Financial
- Banks
- Open Banking
- CDR
- Consumer Banking
- Australia
- Mutual Bank
- Product Reference Data

## Timestamps

- **Created:** 2026-07-20
- **Modified:** 2026-07-20

## APIs

### Police Bank CDR Product Reference Data API

Public, unauthenticated Product Reference Data (PRD) API required of every Australian ADI under the Consumer Data Right. Serves machine-readable product details (rates, fees, features, eligibility) for Police Bank's transaction and savings accounts, term deposits, residential mortgages, personal loans, and credit/charge cards. Confirmed live (HTTP 200, `x-v: 3`, 16 products across 5 categories).

- **Human URL:** [https://www.policebank.com.au/open-banking](https://www.policebank.com.au/open-banking)
- **Base URL:** `https://public.cdr.prd.policebank.com.au/cds-au/v1/banking`

#### Tags

- Open Banking
- CDR
- Product Reference Data
- Banking
- Australia

#### Properties

- [Documentation](https://www.policebank.com.au/open-banking)
- [API Reference](https://consumerdatastandardsaustralia.github.io/standards/#get-products)
- [OpenAPI](openapi/police-bank-cds-banking-products-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

## Common Properties

- [Website](https://www.policebank.com.au/)
- [Documentation](https://www.policebank.com.au/open-banking)
- [Privacy Policy](https://www.policebank.com.au/privacy-policy)
- [Support](https://www.policebank.com.au/contact-us)

## Notes

- **CDR PRD confirmed live:** `https://public.cdr.prd.policebank.com.au/cds-au/v1/banking/products` (HTTP 200, `x-v: 3`).
- **Public base URI source:** CDR Register Get Data Holder Brands Summary API (brandName "Police Bank", ABN 95087650799).
- **No proprietary developer portal or Up-style personal-banking API** is published; the only public developer surface is the CDR PRD API.
- **Spec provenance:** the harvested OpenAPI is the shared DSB Consumer Data Standards CDR Banking API (3.0.3, v1.36.0) — the standard the PRD endpoint conforms to, not a Police Bank-proprietary contract.

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
