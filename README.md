# US LLC Formation Fees Dataset

**51 US jurisdictions (50 states + DC)** with real, verified LLC formation costs for 2026.

Each row: a state's filing fee, annual report fee, franchise tax, and the Secretary of State URL where you can verify the data.

This is the open-data dataset powering [llcformationcost.com](https://llcformationcost.com) — the free LLC formation cost calculator operated by Ordertoai LLC.

## Files

- `states.csv` — 51 rows, CSV format
- `states.json` — same data, structured JSON with additional metadata
- `methodology.md` — full methodology + source citations
- `CITATION.txt` — how to cite this dataset academically

## Schema

| Column | Type | Description |
|---|---|---|
| `code` | string | 2-letter postal code (`CA`, `TX`, `DC`, etc.) |
| `name` | string | Full state name |
| `filingFee` | number | One-time state filing fee (USD) for Articles of Organization |
| `filingForm` | string | Official form name (varies by state) |
| `firstYearAnnualReportFee` | number | Year-1 report fee (separate because some states delay billing) |
| `annualReportFee` | number | Ongoing annual report fee |
| `annualReportCadence` | string | `annual` / `biennial` / `decennial` / `none` |
| `franchiseTaxYearOne` | number | First-year franchise tax (some states grant year-1 exemptions) |
| `franchiseTaxOngoing` | number | Ongoing annual franchise tax |
| `sosUrl` | string | Secretary of State filing URL for verification |

## Sample rows

```csv
AK,Alaska,250,Articles of Organization (Form 08-484),0,100,biennial,0,0,https://www.commerce.alaska.gov/...
AL,Alabama,200,Certificate of Formation,50,50,annual,50,50,https://www.sos.alabama.gov/...
CA,California,70,Articles of Organization (Form LLC-1),20,20,biennial,800,800,https://www.sos.ca.gov/...
```

## Use cases

- Building an LLC formation cost calculator (the source for ours)
- Comparing state costs for entity-formation decisions
- Tax research and entity-structure analysis
- Academic / regulatory research
- Founder tools and incorporation services

## License

CC BY 4.0 — free to use, modify, redistribute with attribution to [llcformationcost.com](https://llcformationcost.com).

## See it live

Browse the full calculator (with state-by-state comparison, foreign-LLC math, S-corp election calculator, registered agent comparator, NY publication cost calculator) at **[llcformationcost.com](https://llcformationcost.com)**.

## Methodology

Each row was verified against the state's Secretary of State website on the date noted in `methodology.md`. Re-verification cadence: quarterly. See `methodology.md` for the full source-citation chain.

Primary sources:
- Each state's Secretary of State public website
- IRS Publication 3402 (Taxation of Limited Liability Companies)
- FinCEN BOI reporting guidance

## Maintainer

This dataset is operated by **Ordertoai LLC** (Texas LLC). Site: [llcformationcost.com](https://llcformationcost.com). Wikidata: [Q139583566](https://www.wikidata.org/wiki/Q139583566).

## Not legal or tax advice

This data is provided for informational purposes only. State filing fees, franchise taxes, and FinCEN deadlines change. Verify current data with the state's Secretary of State, IRS, or a licensed attorney/CPA before relying on it for binding decisions. See [the full disclaimer](https://llcformationcost.com/disclaimer/).

## Versions

| Version | Date | States | Notes |
|---|---|---|---|
| 1.0 | 2026-05-12 | 51 | Initial public release |
