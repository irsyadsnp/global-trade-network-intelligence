# ICIO 2026 Metadata Review — Follow-up

**Review date:** 2026-11-26  
**Official source:** https://www.oecd.org/en/data/datasets/inter-country-input-output-tables.html  
**Status:** Landing-page review complete; Annex/ReadMe file contents and data files not yet inspected.

## 1. What the official page exposes

The OECD ICIO landing page currently lists a 2026 release in two forms:

- Regular ICIO
- Extended ICIO

For the 2026 regular release, the page lists:
- Annex
- ReadMe
- 1995–1999
- 2000–2004
- 2005–2009
- 2010–2014
- 2015–2019
- 2020–2024

For the extended release, the page lists the same six five-year periods, with additional economy-split labels for later groups.

The page states that the regular ICIO covers 95 economies: 83 individual countries and 12 regions separated from the former Rest of the World aggregate. The remaining Rest of the World is a residual for a handful of unallocated territories. The extended version covers the same economies but splits China and Mexico to account for firm heterogeneity.

The OECD also states that 2026 ICIO is available in the earlier country-and-industry format, while RData files for all versions can be requested by email from ICIO-TiVA.Contact@oecd.org.

## 2. Important distinction: landing-page metadata versus file-level metadata

The public landing page identifies the release, economy coverage, format family, and time-block labels. It does **not** expose enough readable information in the page text to establish all file-level details.

The following remain unverified until the Annex, ReadMe, and at least one data file are opened directly:

- Exact industry count and complete industry code list.
- Exact matrix/table names and CSV filenames inside each archive.
- Row and column conventions.
- Units, currency, and valuation basis.
- Treatment of taxes, margins, imports, exports, and final demand components.
- Exact archive sizes and checksums.
- Whether every five-year archive contains all years in its label and whether there are special exceptions.
- Dataset-specific licensing or third-party restrictions.

Do not infer these details from older ICIO editions or third-party software packages.

## 3. Access-route decision

The official landing page is the authoritative starting point. It exposes links for the Annex, ReadMe, and each period group, but the accessible text extraction used for this review did not reveal the actual target URLs for those links.

Therefore, no guessed download URL has been recorded and no file download is claimed.

The next access action is to open the OECD page in a normal browser and use the actual 2026 regular ICIO links. If the files are not directly downloadable, request the RData distribution and sample code from the official OECD contact address listed on the page.

## 4. Current-price versus volume analysis

Do not treat nominal/current-price ICIO values as real-volume measures. Price changes can affect observed edge weights and temporal network comparisons.

The OECD has separately described a PYP (previous-year-price) ICIO framework for volume-based analysis. This is a distinct analytical product and should not be silently substituted for the regular current-price ICIO tables.

For the initial project:
- Use the regular ICIO release for structural and nominal-flow analysis only after its valuation basis is confirmed in the ReadMe.
- If the research question requires real-volume change, assess the OECD PYP ICIO dataset as a separate candidate and document its scope and compatibility.
- Avoid interpreting changes in nominal edge weights as changes in physical quantities.

## 5. Technical review status

| Item | Status |
|---|---|
| Official 2026 landing page verified | Complete |
| Regular versus Extended distinction recorded | Complete |
| 95 economy coverage recorded | Complete |
| Six five-year group labels recorded | Complete |
| Annex contents inspected | Pending |
| ReadMe contents inspected | Pending |
| Industry classification verified | Pending |
| Table schema verified | Pending |
| Units and valuation basis verified | Pending |
| File sizes and checksums recorded | Pending |
| Sample archive downloaded and integrity-tested | Pending |
| Dataset-specific reuse conditions checked | Pending |

## 6. Decision

**Keep OECD ICIO 2026 regular as the preferred primary candidate, but do not yet freeze it as the validated analytical dataset.**

The landing-page review supports conceptual relevance and broad coverage. It does not replace inspection of the Annex, ReadMe, and data files.

## 7. Sources

- OECD, *Inter-Country Input-Output tables*: https://www.oecd.org/en/data/datasets/inter-country-input-output-tables.html (accessed 2026-11-26).
- OECD, *Global value chain data across trade, multinationals and services*: https://www.oecd.org/en/data/datasets/global-value-chain-data-across-trade-multinationals-and-services.html (accessed 2026-11-26). This is a related but distinct OECD product; its PYP/current-price descriptions must not be treated as direct metadata for every ICIO archive.
- OECD, *Trends in Global Value Chains*: https://www.oecd.org/en/publications/trends-in-global-value-chains_8217c2ff-en.html (accessed 2026-11-26).

**No Annex or ReadMe file contents have been verified in this follow-up, and no ICIO data file has been downloaded.**
