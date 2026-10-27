# Data dictionary and provenance
**Original project: April 2021 · Documentation update: October 27, 2026**

## Fields used in the historical Toronto notebook

| Field | Type | Meaning / expected check |
|---|---|---|
| PostalCode | Text | Toronto postal prefix; retain as text and check uniqueness after consolidation |
| Borough | Text | Borough label; exclude unassigned boroughs |
| Neighborhood | Text | Neighborhood name or consolidated names; missing values fall back to borough |
| Latitude | Number | Neighborhood representative latitude; -90 to 90 |
| Longitude | Number | Neighborhood representative longitude; -180 to 180 |
| Neighborhood Latitude | Number | Neighborhood latitude carried into venue records |
| Neighborhood Longitude | Number | Neighborhood longitude carried into venue records |
| Venue | Text | Provider venue name; names alone are not unique identifiers |
| Venue Latitude | Number | Venue latitude |
| Venue Longitude | Number | Venue longitude |
| Venue Category | Text | Venue category selected by the historical retrieval function |

## Historical inputs

| Input | Evidence in repository | Reproduction requirement |
|---|---|---|
| Toronto postal-code table | Wikipedia URL and HTML parser in notebook | Check schema and preserve a dated source snapshot where permitted |
| Coordinate CSV | Local Geospatial_Coordinates.csv reference | Recover the original file and source attribution; it is not bundled |
| Venue observations | Foursquare v2 explore request function | Verify compatible access, response schema, and redistribution terms |
| New York geography / venues | Part of cross-city study description | Recover inputs and executable ingestion before claiming a complete rerun |

## Required fields for modernization

Add city, neighborhood_id, source_name, source_url, retrieved_at, source_vintage, geographic_unit, venue_id where available, search_radius_m, collection_status, and venue_count. These are proposed fields, not existing dataset columns.

Use city-qualified identifiers to prevent identically named neighborhoods in different cities from being merged. A failed request must not become an all-zero venue profile.

## Feature and output contracts

A feature table should contain one row per city-qualified neighborhood and one numeric category column per shared taxonomy entry. Record normalization and missing-data policy.

Model outputs should include neighborhood_id, cluster_id, retained_component_count, model_run_id, and a coverage flag. A similarity result should identify its distance metric and feature space.

## Availability and rights

The repository does not bundle a complete cross-city analysis dataset. Original source dates and redistribution permissions must be established before adding snapshots. Public accessibility is not itself a redistribution license.
