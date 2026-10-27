# Business case
**Original project: April 2021 · Enzo Safadi**  
Documentation update: October 27, 2026.

## Decision problem

Someone moving between Toronto and New York may want a shortlist of neighborhoods with familiar amenities. A location analyst may want to compare local venue mixes before conducting deeper market research. Broad city-level impressions are too coarse for either task.

The project investigates whether neighborhood venue profiles can provide a repeatable starting point for this comparison.

## Intended users and decisions

| User | Decision supported | Additional evidence required |
|---|---|---|
| Relocation researcher | Shortlist areas with a similar amenity mix | Housing costs, commute, accessibility, personal needs |
| Location analyst | Identify comparable areas for further research | Demand, rent, zoning, competition, site visits |
| Urban-data analyst | Explore patterns across city datasets | Coverage checks, geographic comparability, time alignment |

## Proposed decision workflow

Choose an origin neighborhood, compare category profiles, inspect similar groups on a map, review data coverage and collection dates, then produce a research shortlist. These are proposed application behaviors; the archive does not implement a user-facing recommendation service.

## Scope of the academic study

Geographic preparation, venue-category representation, dimensionality reduction, neighborhood clustering, and geographic interpretation. The original report and presentation provide the historical narrative; the available notebook is a partial implementation.

## Value hypothesis

A consistent comparison may reduce manual research and make the basis of a shortlist easier to explain. No time savings, revenue improvement, relocation success rate, or commercial return has been measured here.

## Criteria for a future working version

- Every displayed neighborhood has a stable city-qualified identifier.
- Each ranking shows the underlying factors and data date.
- Sparse or missing venue data produces a visible coverage flag.
- A reviewer can reproduce the output from documented inputs.
- Users can inspect why two neighborhoods were considered similar.
- A shortlist includes limitations and required follow-up research.

## Portfolio contribution

Demonstrates problem framing, geographic data preparation, analytical communication, and an unsupervised-learning design. Production engineering and end-to-end reproducibility remain development work.
