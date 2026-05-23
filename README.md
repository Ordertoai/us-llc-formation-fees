# 2026 LLC Formation Cost Dataset

Open dataset of LLC formation costs across 51 US jurisdictions, sourced
from each state's Secretary of State website + IRS guidance. Released under
**CC BY 4.0** — free to use commercially, with attribution.

## Coverage

51 jurisdictions (50 states + DC where data is available).
Last verified: **2026-05-23**.

## Schema

| Column | Type | Description |
|---|---|---|
| `code` | string | Two-letter state postal code (e.g., `CA`, `TX`, `DC`). |
| `name` | string | Full state name. |
| `filing_fee_usd` | number | One-time domestic LLC filing fee charged by the SOS. |
| `filing_form` | string | Form name or number used to register the LLC. |
| `first_year_annual_report_fee` | number | Annual report fee for year 1. |
| `annual_report_fee` | number | Recurring annual report fee. |
| `annual_report_cadence` | string | One of `annual`, `biennial`, `decennial`, `annual-info-only`, `none`. |
| `franchise_tax_year_one` | number | First-year minimum LLC franchise/privilege tax (USD). |
| `franchise_tax_ongoing` | number | Ongoing annual franchise tax minimum (USD). |
| `processing_days_standard` | number | Typical online processing time (business days). |
| `processing_days_expedite` | number | Expedited processing time (business days). |
| `expedite_fee` | number | Expedite fee (USD); 0 if not available. |
| `publication_required` | boolean | Whether newspaper publication is required (NY, AZ, NE only). |
| `publication_est_cost` | number\|null | Estimated publication cost where required, USD. |
| `sos_url` | string | Canonical Secretary of State URL. |
| `last_verified_date` | string (YYYY-MM-DD) | Date the entry was last verified against the SOS. |

## Files

- [`states.csv`](./states.csv) — flat CSV (recommended for analysis)
- [`states.json`](./states.json) — original nested JSON

## How to cite

Per CC-BY-4.0, attribution is required when reusing the data:

> Baidi, A. (2026). *2026 LLC Formation Cost Dataset*.
> llcformationcost.com. Available at https://github.com/Ordertoai/us-llc-formation-fees.
> Licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

The interactive calculator built on this data: <https://llcformationcost.com>

## Methodology

Each entry verified directly against the issuing state's Secretary of State
or DCRA/DLCP website. AI-sourced entries are tagged with `verifiedSource:
"gemini-grounded-search-{date}"` in the original JSON. Re-verified
quarterly.

## License

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) — share + adapt
freely, attribution required.
