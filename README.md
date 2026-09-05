# Export-Import Bank of the United States (export-import-bank-of-the-united-states)

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

The U.S. Export-Import Bank (EXIM) is the official export credit agency of the United States federal government. It assists in financing and facilitating U.S. exports of goods and services by providing export credit insurance, working capital guarantees, loan guarantees and direct loans to help American businesses compete in the global marketplace.

**EXIM operates no public API.** Its Socrata/SODA open data portal at `data.exim.gov` was decommissioned on 2023-09-14 by EXIM's own announcement, and the host no longer resolves in DNS. What remains is a Project Open Data v1.1 (DCAT-US) catalog pointing at a quarterly CSV of every authorization approved since FY2007, distributed through Data.gov.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/export-import-bank-of-the-united-states/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/export-import-bank-of-the-united-states/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Producing

## Tags

- Export
- Federal Government
- Finance
- Import
- Open Data
- Trade Finance

## Timestamps

- **Created:** 2024-07-11
- **Modified:** 2026-09-04

## APIs

### EXIM Open Data Catalog

EXIM's entire programmatic open-data footprint: a Project Open Data v1.1 (DCAT-US) catalog at `data.json` listing one public dataset — every EXIM authorization approved from 10/01/2006 to the current reporting quarter — with a quarterly CSV distribution and a PDF data dictionary. Anonymous HTTPS GET, no key, no quota. This is file distribution, not a query API. The CSV filename carries the fiscal quarter, so consumers must re-read `data.json` rather than pinning the download URL.

- **Human URL:** [https://www.exim.gov/open-government-data](https://www.exim.gov/open-government-data)
- **Base URL:** `https://img.exim.gov/s3fs-public/dataset/vbhv-d8am/`
- **Operator:** institution (EXIM)

#### Properties

- [Documentation](https://www.exim.gov/open-government-data)
- [Data Catalog](data-catalog/export-import-bank-of-the-united-states-data-catalog.yml)
- [Project Open Data catalog (data.json)](https://img.exim.gov/s3fs-public/dataset/vbhv-d8am/data.json) — [Project Open Data v1.1](https://project-open-data.cio.gov/v1.1/schema)
- [Data.gov listing](https://catalog.data.gov/organization/exim)

### EXIM Digital Archives (CONTENTdm / IIIF)

26 collections of EXIM's historical record — annual reports, press releases, board materials, executive orders, oral histories, reports to Congress — served over anonymous JSON endpoints and IIIF Presentation API 2.0 manifests at an `exim.gov` address.

**Operator attribution:** `www.digitalarchives.exim.gov` is a CNAME to `cdm16645.contentdm.oclc.org`, and the IIIF manifests resolve their own `@id` to that OCLC host. EXIM is the tenant and owns the content; the contract is OCLC CONTENTdm's product, not an API EXIM engineered.

- **Human URL:** [https://www.digitalarchives.exim.gov/](https://www.digitalarchives.exim.gov/)
- **Base URL:** `https://www.digitalarchives.exim.gov/digital/`
- **Operator:** vendor (OCLC CONTENTdm)

#### Properties

- [API Reference](https://help.oclc.org/Metadata_Services/CONTENTdm/Advanced_website_customization/API_Reference/CONTENTdm_API)
- [IIIF Presentation API 2.1](https://iiif.io/api/presentation/2.1/)

## Artifacts

- [Data catalog](data-catalog/export-import-bank-of-the-united-states-data-catalog.yml) — EXIM's DCAT-US catalog, saved verbatim
- [Conformance](conformance/export-import-bank-of-the-united-states-conformance.yml) — Project Open Data v1.1, DCAT, IIIF 2.0
- [Lifecycle](lifecycle/export-import-bank-of-the-united-states-lifecycle.yml) — the dated `data.exim.gov` decommissioning
- [Plans](plans/export-import-bank-of-the-united-states-plans-pricing.yml) — `plan_count: 0`, free public data
- [Rate limits](rate-limits/export-import-bank-of-the-united-states-rate-limits.yml) — `limit_count: 0`, no surface to limit
- [Authentication](authentication/export-import-bank-of-the-united-states-authentication.yml) — anonymous everywhere public
- [Well-known probe](well-known/export-import-bank-of-the-united-states-well-known.yml) — nothing served, on seven hosts
- [Domain security](security/export-import-bank-of-the-united-states-domain-security.yml)
- [Vulnerability disclosure](security/export-import-bank-of-the-united-states-vulnerability-disclosure.yml) — real VDP, not machine-discoverable
- [Agentic access](agentic-access/export-import-bank-of-the-united-states-agentic-access.yml)
- [llms.txt](llms/export-import-bank-of-the-united-states-llms.txt)

`_quarantine/` holds a fabricated OpenAPI and everything derived from it, removed from the scored tree on 2026-09-04. See [`_quarantine/NOTE.md`](_quarantine/NOTE.md).

## Common Properties

- [Website](https://www.exim.gov/)
- [Portal](https://eximonline.exim.gov/)
- [Getting Started](https://www.exim.gov/open-government-data)
- [Security / Vulnerability Disclosure Policy](https://www.exim.gov/vulnerability-disclosure-policy)
- [Blog](https://grow.exim.gov/blog)
- [News](https://www.exim.gov/news)
- [Support](https://www.exim.gov/contact/contact-form)
- [Privacy Policy](https://www.exim.gov/privacy-and-security-policy)
- [Terms of Service](https://www.exim.gov/policies)
- [LinkedIn](https://www.linkedin.com/company/eximbankus)
- [YouTube](https://www.youtube.com/user/EximBankofUS)
- [Twitter / X](https://x.com/eximbankus)
- [Facebook](https://www.facebook.com/eximbankus/)
- [Instagram](https://www.instagram.com/eximbankus/)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
