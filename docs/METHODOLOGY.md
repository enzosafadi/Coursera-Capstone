# Methodology and evidence
**Original project: April 2021 · Documentation review: October 27, 2026**

## Evidence inventory

| Artifact | Observed role | Verification boundary |
|---|---|---|
| Introductory notebook | NumPy import and course greeting | Does not implement analysis |
| Toronto notebook | Postal-table parsing, cleaning, coordinate merge, mapping code, venue-request function | Partial workflow; no complete cross-city model |
| Report PDF | Original analytical report | Retained; numerical conclusions not revalidated in this documentation update |
| Presentation and dataset PDF | Historical communication and data context | Retained as original artifacts |

The previous README described 250 features, 150 PCA components, and five clusters. Those figures are not presented as newly verified results. A future reproducible run must establish its own counts and diagnostics.

## Intended analytical procedure

1. **Geography:** clean borough and neighborhood labels, consolidate postal-code records, validate coordinate coverage, and preserve geographic-unit definitions.
2. **Venue collection:** use one documented provider and category taxonomy, with comparable radii, limits, collection windows, and pagination handling.
3. **Feature construction:** deduplicate venue observations and calculate category proportions per city-qualified neighborhood. Keep observation counts alongside proportions.
4. **Shared feature space:** align category columns across cities. Distinguish a genuinely absent category from a failed or missing collection.
5. **PCA:** document centering/scaling choices and explained variance. Select the component count from the actual data and objective; do not hard-code the historical count.
6. **Clustering:** evaluate feasible values of k using inertia, silhouette scores, stability across seeds, cluster sizes, and interpretability. Record random seed and n_init.
7. **Interpretation:** inspect category distributions and map outputs. Cluster identifiers have no ordinal meaning.
8. **Sensitivity:** vary collection radius, feature preprocessing, PCA threshold, and k. Report unstable assignments.

## Known implementation gaps

The Toronto notebook includes:
- Absolute Windows input and Excel-output paths.
- Package-install shell commands inside notebook cells.
- A legacy pandas json_normalize import.
- Nominatim use without a corresponding import in the visible code.
- CLIENT_ID, CLIENT_SECRET, VERSION, and LIMIT references without definitions in the checked-in workflow.
- A historical Foursquare v2 response schema with no timeout, retry, status check, or missing-group handling.
- No complete New York ingestion, shared feature table, fitted PCA, or clustering evaluation.

The notebooks were inspected as source; their external calls were not executed.

## Bias and validity

Postal regions and named neighborhoods are not necessarily comparable geographic units. Provider coverage, tourism, category granularity, and sparse observations can dominate similarity. Venue presence is not footfall, consumer spending, or commercial success. Treat missing coverage as uncertainty rather than a zero-demand signal.

## Evidence needed for future results

Retain the input manifest, provider terms, collection dates, geographic definitions, row counts, exclusion log, package lock, model settings, diagnostics, and generated outputs. Publish only data allowed by its source terms.
