# Police Bank (police-bank)

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
