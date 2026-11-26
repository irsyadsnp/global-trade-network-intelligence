# OECD ICIO Source Feasibility Audit

**Audit date:** 2026-11-26  
**Source:** OECD Inter-Country Input-Output (ICIO) tables  
**Official dataset page:** https://www.oecd.org/en/data/datasets/inter-country-input-output-tables.html  
**Audit status:** Preliminary source-level review; files and detailed metadata have not yet been inspected.

## 1. Findings verified from the OECD landing page

The OECD page currently lists a **2026 ICIO release** with two variants:

- **Regular ICIO:** 95 economies, consisting of 83 individual countries and 12 regional aggregates. The residual Rest of the World category represents a small number of territories not allocated elsewhere.
- **Extended ICIO:** the same economy coverage, with China and Mexico split to account for firm heterogeneity. The OECD states that this extended version is used to generate its GVC-related indicators.

The 2026 release is presented in country-and-industry format. The regular release is divided into six five-year file groups: 1995–1999, 2000–2004, 2005–2009, 2010–2014, 2015–2019, and 2020–2024. The page states that RData files for all versions can be provided upon request.

The OECD describes ICIO as mapping production, consumption, and investment within economies, as well as international trade in goods and services, by country and economic activity.

## 2. Preliminary suitability assessment

**Recommendation: use the 2026 regular ICIO as the primary candidate, subject to file-level validation.**

Reasons:
- It provides a long annual span (1995–2024) suitable for structural and temporal analysis.
- Its country-and-industry representation aligns with the project's intended country-industry network.
- The regular version avoids the additional firm-heterogeneity split in China and Mexico, simplifying the initial node schema.
- The 2026 release is the current release listed on the OECD source page as of the audit date.

This is a source-selection recommendation, not confirmation that the files are already validated or that every variable is suitable for every research question.

## 3. Coverage and comparability cautions

- The 95 economy units include regional aggregates; they must not be treated as 95 sovereign countries.
- The Rest of the World residual is not equivalent to a fully observed country.
- The extended version changes the representation of China and Mexico. Do not combine regular and extended observations in one network without a carefully defined harmonization procedure.
- A 1995–2024 time span does not by itself establish that every country-industry cell is equally comparable across all years.
- Confirm industry codes, labels, number of industries, table dimensions, units, valuation basis, and accounting identities from the 2026 Annex and ReadMe before constructing the graph.
- Confirm whether the 2023–2024 observations have any estimation or projection status in the specific ICIO release documentation. Do not assume all years have identical source maturity.

## 4. Access and format

The OECD page lists the 2026 regular ICIO files in five-year groups and provides an Annex and ReadMe. It also states that RData files can be provided for all versions upon request.

The page does not, by itself, establish the exact file size, compression format, download URL stability, or whether the full set can be fetched reliably by an automated script. These must be tested before designing the acquisition pipeline.

## 5. Reuse terms and data governance

OECD general data terms state that, except where additional restrictions or third-party ownership apply, data may be downloaded, copied, adapted, distributed, and shared for commercial or non-commercial purposes with appropriate attribution.

However, OECD also explicitly warns that particular datasets may have additional restrictions or third-party rights. Therefore:

- Record the dataset-specific metadata and any source/ownership notes in the downloaded Annex or ReadMe.
- Preserve the required OECD citation and access date.
- Do not redistribute raw ICIO files in this repository until the dataset-specific restrictions and third-party contributions have been checked.
- The repository's MIT license does not apply to OECD data.

General terms: https://www.oecd.org/en/about/terms-conditions.html

## 6. Preliminary decision matrix

| Criterion | Preliminary result | Status |
|---|---|---|
| Official source | OECD dataset landing page | Pass |
| Current release identified | 2026 regular and extended ICIO listed | Pass |
| Longitudinal coverage | 1995–2024 listed for regular ICIO | Pass |
| Country-industry representation | Explicitly stated by OECD | Pass |
| Economy coverage | 95 units: 83 countries + 12 regions | Pass with aggregation caveat |
| Download format and file integrity | Not yet tested | Pending |
| Detailed industry classification | Annex/ReadMe not yet inspected | Pending |
| Units and valuation basis | ReadMe not yet inspected | Pending |
| Dataset-specific reuse restrictions | Must be checked in metadata/source notes | Pending |
| Reproducible acquisition route | Not yet tested | Pending |

## 7. Next audit actions

1. Retrieve the 2026 regular ICIO Annex and ReadMe.
2. Inspect all six file links and determine the actual file format, size, and direct download URLs.
3. Verify the industry list, economy identifiers, table dimensions, units, and valuation basis.
4. Inspect release notes for revisions and any special treatment of 2023–2024.
5. Test downloading one representative year-group file and verify its checksum and archive integrity.
6. Confirm dataset-specific reuse conditions before storing or redistributing any raw data.
7. Only after these checks, freeze the dataset version and create the acquisition manifest.

## 8. Sources

- OECD, *Inter-Country Input-Output tables*: https://www.oecd.org/en/data/datasets/inter-country-input-output-tables.html (accessed 2026-11-26).
- OECD, *Terms & Conditions*: https://www.oecd.org/en/about/terms-conditions.html (accessed 2026-11-26).

**Conclusion:** OECD ICIO 2026 regular is the preferred primary dataset candidate. It passes the initial conceptual and coverage review, but acquisition and file-level validation remain outstanding. No data have been downloaded and no empirical analysis has been performed.
