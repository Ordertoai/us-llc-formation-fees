# 2026 LLC Cost Index — Methodology

**Last updated:** 2026-04-28
**Maintainer:** Aissam Baidi
**License:** CC BY 4.0 (citation + backlink required for any reuse)

## What this dataset contains

51 jurisdictions (US states + DC where applicable) with the following fields per entry:

| Field | Type | Description |
|---|---|---|
| `code` | string | Two-letter postal code (e.g., `CA`, `TX`, `DC`) |
| `name` | string | Full state name |
| `filingFee` | number | One-time state filing fee in USD |
| `filingForm` | string | Official form name (e.g., "Articles of Organization") |
| `firstYearAnnualReportFee` | number | Year-1 report fee (separate because some states delay year-1 billing) |
| `annualReportFee` | number | Ongoing annual/biennial/decennial report fee |
| `annualReportCadence` | string | One of `annual` | `biennial` | `decennial` | `none` |
| `franchiseTaxYearOne` | number | First-year franchise tax (some states grant a year-1 exemption) |
| `franchiseTaxOngoing` | number | Recurring franchise tax (annual flat amount) |
| `sosUrl` | string | Primary source URL (Secretary of State website) |

## Sourcing

Every entry is verified directly against the issuing state's Secretary of State office. The `sosUrl` field for each state contains the exact primary source URL used.

## Verification cadence

Quarterly. Each entry has a `lastVerifiedDate` (in the JSON file but not the flat CSV).

## Versioning

Each quarterly refresh updates the dataset in place. The version corresponds to the calendar quarter of the most recent verification.

Current version: **2026-Q2**

## Known gaps

- Local (city/county) license fees are NOT included — these vary by ZIP code and are out of scope for a state-level dataset.
- "Publication requirement" states (NY, AZ, NE) have additional one-time costs not captured in `filingFee` — see each state's individual page on llcformationcost.com for the full breakdown.
- Cost of registered-agent service is NOT included (varies by provider, typically $100-150/year).
