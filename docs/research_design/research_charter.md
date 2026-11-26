# Research Charter

**Project:** Global Trade Network Intelligence  
**Status:** Provisional research design — pending dataset feasibility audit  
**Version:** 0.1.0

## 1. Research purpose

Describe and evaluate the structure, concentration, and temporal evolution of international production and trade relationships using reproducible statistical and network methods.

The project is designed as an observational, quantitative study. Its initial purpose is descriptive and structural. Causal interpretations are outside the scope unless a later research question, identification strategy, and suitable data support them.

## 2. Primary analytical direction

The primary analytical direction is an inter-country, inter-industry production network constructed from an OECD Inter-Country Input-Output (ICIO) release, subject to verification of the release structure and documentation.

Bilateral merchandise trade data from UN Comtrade may be used as a separate complementary network. It must not be merged conceptually with ICIO flows without an explicit mapping and justification.

The project will preserve these as distinct analytical objects:

- **ICIO production/input network:** relationships represented by inter-country and inter-industry input-output transactions.
- **Bilateral merchandise-trade network:** reported flows of goods between reporter and partner economies, optionally disaggregated by product and period.

## 3. Research objectives

1. Characterize the topology and weighted structure of global inter-country production relationships.
2. Identify economies and industries with structurally prominent positions under clearly specified network measures.
3. Quantify concentration and dependence patterns at country and industry levels.
4. Evaluate whether detected communities are stable across time, aggregation choices, and network specifications.
5. Measure structural change over time while separating genuine change from changes in coverage, classifications, and source revisions.

## 4. Core research questions

**RQ1 — Network structure:** What are the principal structural properties of the global inter-country production network?

**RQ2 — Structural position:** Which countries and industries occupy prominent positions, and how do rankings vary across network measures and specifications?

**RQ3 — Concentration and dependence:** How concentrated are production-input relationships, and how dependent are economies on a limited set of foreign suppliers or destinations?

**RQ4 — Communities:** Do communities or clusters emerge in the network, and how persistent are they across periods and methodological choices?

**RQ5 — Temporal change and robustness:** How does network structure change over the observed period, and which findings remain robust to alternative definitions, thresholds, and aggregation levels?

These questions may be narrowed after the dataset audit. No result is presumed by the wording of the questions.

## 5. Units of analysis and network representation

The intended primary units are country-industry pairs and directed relationships between them. The exact unit must be aligned with the selected ICIO release.

A network specification must document, before metric calculation:

- Node identity and level: country, industry, or country-industry.
- Edge direction: the economic meaning of source and target nodes.
- Edge weight: the exact transaction or flow quantity represented.
- Time unit: annual or another documented period.
- Aggregation: treatment of industries, countries, regional aggregates, and totals.
- Inclusion rules: treatment of zero, missing, suppressed, and negative values, where applicable.

A directed edge must not be interpreted as a generic measure of dependence until its direction and economic meaning are defined. In particular, supplier-to-user and user-to-supplier orientations answer different questions.

## 6. Candidate data sources

### Primary candidate — OECD ICIO

Official landing page: https://www.oecd.org/en/data/datasets/inter-country-input-output-tables.html

Use case: inter-country and inter-industry production/input relationships.

Before selection, verify the release version, years, economy and industry coverage, table layout, units, valuation basis, documentation, revisions, and terms of use.

### Complementary candidate — UN Comtrade

Official portal: https://comtradeplus.un.org/

Use case: bilateral merchandise-trade relationships and potential product-level extensions or comparisons.

Before use, verify reporter/partner coverage, commodity classification, flow definitions, reporting periods, revision policy, access limits, and terms of use.

The two sources measure different economic constructs. Any comparison must state the conceptual and statistical limitations of the mapping.

## 7. Analytical plan

The planned sequence is:

1. Audit source documentation, coverage, data structure, access, and reuse terms.
2. Define the analytical population, unit of analysis, and network representation.
3. Validate identifiers, classifications, units, missingness, duplicates, and accounting consistency.
4. Produce descriptive statistics and exploratory visualizations.
5. Construct and inspect weighted directed networks.
6. Calculate suitable centrality, concentration, and community measures.
7. Compare network structures across time where coverage is sufficiently comparable.
8. Conduct sensitivity and robustness analyses.
9. Consider predictive or machine-learning methods only if they address a distinct, testable question and a defensible validation design is available.

## 8. Validity and interpretation safeguards

- Centrality is a property of a specified graph, not a universal ranking of economic power.
- High edge weight, high centrality, and high dependence are distinct concepts.
- Community detection is algorithm- and resolution-dependent; detected groups are not automatically geopolitical blocs.
- Comparisons over time require stable definitions or explicit harmonization.
- Missing or changing reporting coverage can create apparent structural change.
- Descriptive network patterns do not establish causal effects.
- Sensitivity analyses should vary defensible assumptions rather than search for a preferred result.

## 9. Inclusion and exclusion boundaries

**Included initially**
- Cross-border production/input relationships represented in the selected ICIO release.
- Country and industry structural summaries.
- Descriptive network, concentration, community, and temporal analysis.
- Complementary bilateral goods-trade analysis only if data feasibility and conceptual fit are established.

**Excluded initially**
- Causal claims about policy interventions or geopolitical events.
- Financial flows, services trade, and firm-level networks unless a separate data source and research protocol are approved.
- Forecasting as a default objective.
- Combining ICIO and Comtrade observations into one graph without a documented harmonization framework.

## 10. Decision gates

The project may proceed to acquisition only after the primary candidate passes a feasibility review covering:

1. Public or otherwise authorized access.
2. Clear license and reuse conditions.
3. Sufficient temporal and geographic coverage.
4. Available documentation and interpretable variables.
5. A workable file format and reproducible acquisition route.

If the candidate fails a gate, revise the scope or select another source before building the analytical pipeline.

## 11. Current limitations and open decisions

The following remain unresolved until source documentation and files are inspected:

- Exact ICIO release and year coverage.
- Exact country/region and industry classification.
- Variable names, units, and table layout.
- Appropriate direction and aggregation for each network question.
- Treatment of regional aggregates and rest-of-world categories.
- Whether UN Comtrade adds sufficient value to justify a second data pipeline.

No dataset has been downloaded or validated at the time this charter was written. Therefore, all analytical plans are provisional and no empirical findings are claimed.

## 12. Change control

Any material change to research questions, dataset choice, node/edge definitions, inclusion criteria, or primary metrics should be recorded in the project decision log with the rationale and implications for comparability.
