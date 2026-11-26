# Global Trade Network Intelligence

A reproducible data-science research project investigating the structure, dependencies, and evolution of international trade and production networks.

## Research scope

The project studies how economies and industries are connected through cross-border trade and intermediate-input relationships. It will use network science, applied statistics, econometrics, and machine learning where justified by the data.

### Core research questions

1. How is the global trade network structured across countries and industries?
2. Which economies occupy structurally important positions in the network?
3. How concentrated are trade relationships and input dependencies?
4. Do countries form persistent trade communities or blocs?
5. How has the network changed over time, and how sensitive are the findings to alternative network definitions?

## Data strategy

### Primary candidate: OECD Inter-Country Input-Output (ICIO)

Official source: https://www.oecd.org/en/data/datasets/inter-country-input-output-tables.html

ICIO is the primary candidate because it represents inter-country, inter-industry production and input relationships. Before analysis, the project will verify the selected release, coverage, units, industry classification, country/region aggregation, valuation basis, and revision notes against its official documentation.

### Complementary candidate: UN Comtrade

Official source: https://comtradeplus.un.org/

UN Comtrade may be used for bilateral merchandise-trade validation or product-level extensions. Its reporting coverage, classification revisions, API limits, and data availability will be audited before use.

**No dataset has yet been downloaded or validated in this repository.** Dataset versions, licenses/terms, and reproducible acquisition instructions will be recorded before analysis. Raw data files will not be committed unless redistribution is explicitly permitted.

## Planned methods

- Data validation, harmonization, and reproducible transformations
- Directed, weighted network construction
- Degree, strength, betweenness, and eigenvector-based measures, where appropriate
- Community detection and concentration analysis
- Input-output analysis for ICIO-derived questions
- Temporal network comparison
- Sensitivity analysis and robustness checks
- Machine learning only where it answers a clearly defined research question and can be validated without leakage

## Methodological principles

- Distinguish trade flows from input-output relationships; they are related but not interchangeable.
- Define node, edge direction, edge weight, time unit, and aggregation level before calculating network metrics.
- Do not interpret centrality as causal influence or economic importance without a defensible theoretical argument.
- Account for country/industry coverage changes, missing reporters, re-exports, classification changes, and revisions.
- Treat descriptive associations as associations, not causal effects.
- Record data provenance, transformations, assumptions, and limitations.

## Repository status

**Current stage:** Stage 01 — Research foundation.

A provisional research charter is documented in `docs/research_design/research_charter.md`. Dataset selection and validation remain pending. No empirical findings are claimed.

## Planned project structure

```text
.
├── README.md
├── LICENSE
├── .gitignore
├── docs/
│   ├── research_design/
│   ├── data/
│   └── methodology/
├── data/
│   ├── raw/          # excluded from Git
│   ├── interim/      # excluded from Git
│   └── processed/    # excluded from Git unless explicitly approved
├── notebooks/
├── src/
├── tests/
└── outputs/
    ├── figures/
    └── tables/
```

## Reproducibility and data governance

- Keep source data separate from derived data.
- Do not commit credentials, API tokens, or restricted data.
- Preserve original source files and document checksums when permitted.
- Record software versions, parameters, and random seeds.
- Cite the original data providers and comply with their terms of use.

## License

The repository's MIT license applies to original project code and documentation unless otherwise stated. It does **not** relicense third-party datasets or override their terms of use.
