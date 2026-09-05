# Quarantine — fabricated contract removed 2026-09-04

These files were removed from the scored artifact tree by the API Evangelist enrichment
pipeline (STEP 0c ownership / no-fabrication check). They are kept here as evidence, not
as artifacts. **Nothing in this directory is wired into `apis.yml`.**

## What was wrong

`openapi/_original/export-import-bank-of-the-united-states-openapi.yml` was committed on
2026-08-03 with the message *"Add best-effort OpenAPI 3.1 spec generated from
documentation"* — a self-confessed scaffold, never harvested from EXIM. Its
`servers[]` names `https://data.exim.gov`.

Probed 2026-09-04:

| check | result |
|---|---|
| `dig data.exim.gov` | **no A/CNAME record** — host does not resolve |
| `curl https://data.exim.gov/` | `000` — `Could not resolve host` |
| `https://img.exim.gov/s3fs-public/dataset/vbhv-d8am/vbhv-d8am.json` | `200` — EXIM's own archived Socrata metadata states: *"NOTE: EXIM OPEN/Data.gov data is moving to Catalog.Data.gov! Data.EXIM.gov will cease operations effective 9/14/2023."* |
| `https://www.exim.gov/open-government-data` | `200` — EXIM's live Open Data Hub page names only Data.gov; it makes no mention of SODA, Socrata, or any API |

The spec therefore described a surface EXIM decommissioned on **2023-09-14**, on a host
with no DNS, and it was the sole grounding for every derived artifact below.

## What was quarantined

- `openapi/` — the scaffold plus both refined per-tag splits derived from it.
- `collections/` — Postman + OpenCollection files, all derived from the scaffold.
- `authentication/` — the `X-App-Token` apiKey profile, derived from the scaffold's
  Socrata security scheme.
- `plans/` — a Free / Professional / Enterprise pricing scaffold. EXIM is a US federal
  export credit agency; it sells no API plans. The file declared its own values
  "scaffold defaults".
- `rate-limits/` — the same bulk-sweep scaffold, self-declared as placeholder values.

Replacements written by the same pass record the honest measurement instead:
`plans/` (`plan_count: 0`), `rate-limits/` (`limit_count: 0`), `lifecycle/`
(the dated decommissioning), `conformance/`, `well-known/`, `llms/` and
`data-catalog/` (EXIM's real Project Open Data v1.1 catalog).
