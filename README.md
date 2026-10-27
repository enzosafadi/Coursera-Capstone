# Cross-City Neighborhood Clustering
## Toronto & New York Location Intelligence

**An academic data science case study exploring neighborhood similarities through venue patterns, dimensionality reduction, and clustering.**

**Enzo Safadi · Original project: April 2021**  
Repository documentation updated: October 27, 2026.

## Business purpose

Help relocation and location-planning research begin with a structured comparison of neighborhood amenities. The analytical question is: **which neighborhoods in Toronto and New York share similar venue profiles?**

This is an exploratory academic project. Similar amenities do not establish equivalent living conditions, commercial demand, affordability, or investment value.

## Explore the project

| Resource | What it contains |
|---|---|
| [Original analytical report](Report_TheBattleOfNeighborhhods.pdf) | Historical business problem, analysis, and conclusions |
| [Original presentation](The%20Battle%20Of%20Neighborhoods%20Project_Presentation.pptx) | Academic presentation |
| [Original dataset description](The%20Battle%20of%20Neighborhoods_Dataset.pdf) | Historical data context |
| [Business case](docs/BUSINESS_CASE.md) | Intended users, decision workflow, and boundaries |
| [Methodology and evidence](docs/METHODOLOGY.md) | Analytical design and implementation status |
| [Data dictionary](docs/DATA_DICTIONARY.md) | Geographic and venue fields |
| [Setup and reproducibility](docs/SETUP.md) | Environment preparation and known blockers |
| [Development roadmap](docs/ROADMAP.md) | Prioritized modernization and acceptance criteria |

## What is available today

- Original report, dataset-description PDF, and presentation.
- An introductory notebook and a Toronto data-preparation / venue-retrieval notebook.
- Historical notebook outputs illustrating geographic preparation.
- Supporting repository documentation and a suggested dependency manifest.

**Reproducibility status:** the repository is an academic archive with documented modernization work outstanding. The checked-in Toronto notebook does not contain a complete Toronto–New York PCA and clustering pipeline. Importing KMeans is not evidence that clustering runs. The original report remains the reference for historical conclusions; no new model results or business outcomes are claimed in this update.

## Analytical design

1. Prepare neighborhood identities and coordinates.
2. Collect comparable venue-category observations for both cities.
3. Aggregate category frequencies into neighborhood profiles.
4. Fit PCA on a shared feature space.
5. Evaluate candidate cluster counts and fit K-means.
6. Interpret neighborhood groups through category summaries and maps.

Steps 3–6 describe the intended cross-city design, not a newly verified execution of the checked-in notebooks. See [methodology](docs/METHODOLOGY.md).

## Technology

Python, Jupyter, pandas, NumPy, Beautiful Soup, Requests, scikit-learn, Folium, GeoPy, and Matplotlib. Foursquare appears as the historical venue-data provider.

## Start reviewing

The report and presentation can be reviewed directly without running code. To prepare a notebook environment:

```bash
git clone https://github.com/enzosafadi/Coursera-Capstone.git
cd Coursera-Capstone
python -m venv .venv
```

Activate the environment using the instructions in [SETUP.md](docs/SETUP.md), then:

```bash
python -m pip install -r requirements.txt
jupyter notebook
```

These commands prepare an environment; they do not resolve the historical paths, missing data, and legacy API dependencies. No paid API subscription is needed merely to review the archive.

## Repository map

| Path | Role |
|---|---|
| `Capstone Project_1_IBM (1).ipynb` | Introductory course notebook |
| `The Battle of Neighborhoods (Week 1)_Toronto.ipynb` | Historical Toronto preparation and venue-retrieval draft |
| `Report_TheBattleOfNeighborhhods.pdf` | Original report; original filename retained |
| `The Battle Of Neighborhoods Project_Presentation.pptx` | Original presentation |
| `The Battle of Neighborhoods_Dataset.pdf` | Original dataset description |
| `docs/` | Business case, methodology, data dictionary, setup, roadmap |
| `requirements.txt` | Suggested review / modernization dependencies |
| `.gitignore` | Local environments, credentials, and generated-data exclusions |
| `CHANGELOG.md` | Repository documentation changes |

## Interpretation and data boundaries

- Venue similarity is a research signal, not proof of neighborhood quality or business viability.
- Historical venue coverage, geographic units, and collection dates can differ between cities.
- A complete rerun requires recoverable inputs, compatible provider access, and corrected code.
- Third-party data and original academic materials retain their respective rights and terms.
- No production application, validated profitability estimate, or measured client benefit is claimed.

**April 2021 · Academic portfolio project · Enzo Safadi**

## Who it benefits

Location researchers, relocation analysts and students: a historical example of comparing Toronto and New York neighborhood amenities. Current repository contents are an academic archive with reproducibility work outstanding.

These are intended users and benefits, not evidence of adoption or measured customer outcomes.
