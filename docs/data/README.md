# Data Documentation

This folder records dataset provenance and data-quality decisions.

For every source, document:
- Official source and access date
- Dataset title, release/version, and coverage
- Unit of observation, identifiers, and variables
- Geographic and industry classifications
- License, terms of use, and redistribution restrictions
- Known limitations, revisions, and transformations
- Checksums for downloaded files where practical

Do not commit raw or restricted third-party data unless redistribution is explicitly permitted. Never store API keys or credentials in this repository.

## Current source audit

See [OECD ICIO source feasibility audit](icio_source_audit.md) for the preliminary review of the 2026 regular release, coverage, access, reuse terms, and pending validation actions.

Current recommendation: OECD ICIO 2026 regular is the preferred primary candidate. It is not yet approved for analysis or raw-data redistribution; file-level metadata and access still need to be checked.

## Follow-up metadata review

The landing-page findings and outstanding file-level checks are recorded in [ICIO 2026 Metadata Review](icio_2026_metadata_review.md). The Annex, ReadMe, and archives still require direct inspection; no download is claimed.

## Download procedure

Follow the [ICIO 2026 Download and Validation Guide](icio_download_and_validation_guide.md). Download only the Annex, ReadMe, and one 1995–1999 Regular sample block first. Do not acquire all periods until the sample passes validation.
