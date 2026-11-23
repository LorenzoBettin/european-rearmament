# European Rearmament: Spending, Geography and Foreign Arms Dependence

[Read the portfolio case study](https://lorenzobettin.github.io/projects/european-rearmament/)

## Overview

This independent research project investigates three questions:

1. How did real EU-27 military expenditure evolve between 2014 and 2025?
2. How is geographical proximity to Russia associated with national defence expenditure?
3. What do SIPRI major-arms transfer records reveal about EU members' reliance on US-origin and other suppliers?

The study is **descriptive and exploratory**. Cross-country correlations are not causal estimates. SIPRI's **Trend Indicator Value (TIV) reflects the volume of major arms transfers, not their financial value**.

## Methods

Python/Jupyter analysis combining data preparation (pandas, NumPy), GIS processing (GeoPandas), descriptive visualization (Matplotlib) and statistical testing (SciPy, statsmodels).

The notebook reports, among other results:

- EU-27 real military expenditure growth of approximately **104.19%** from 2014–2025 in constant 2024 USD.
- A **Spearman ρ of approximately −0.770** between capital distance from Russia and change in military expenditure as a share of GDP, across 27 EU members.
- A **50.56% share** of recorded EU major-arms import TIV originating in the United States during 2021–2025.

These are results obtained from the data and specifications used in the original notebook and are not causal conclusions.

## File structure

```text
European_Rearmament.ipynb
README.md
.gitignore
data/raw/  # obtain datasets separately; not distributed here
```

## Data sources and reproduction

Obtain the data from the official providers, subject to their own licensing terms:

- [SIPRI Military Expenditure Database](https://www.sipri.org/databases/milex): the analysis references `SIPRI-Milex-data-1949-2025_v1.2.xlsx`.
- [SIPRI Arms Transfers Database](https://www.sipri.org/databases/armstransfers): the analysis references a custom CSV export with recipient, supplier and five-year period tables. Match the filename specified in the notebook or update `arms_file` locally.
- [Eurostat GISCO](https://ec.europa.eu/eurostat/web/gisco): the analysis references `CNTR_RG_01M_2024_4326.geojson`, `URAU_LB_2024_4326_CITIES.geojson` and `URAU_AT_2024.csv`.

Place the downloads in a local `data/raw/` folder, then run the notebook from the repository root. Install dependencies as required by your Python environment, e.g. `pandas`, `numpy`, `geopandas`, `matplotlib`, `scipy`, `statsmodels`, `seaborn`, `openpyxl` and `jupyter`.

Some intermediate results are written into `data/processed/`; this directory is excluded from Git. Reproduction depends on obtaining compatible dataset releases and exports.


## Rights and Attribution

### SIPRI Data

This project uses information from two databases maintained
by the Stockholm International Peace Research Institute (SIPRI).

**Military expenditure data:**

Information from the Stockholm International Peace Research
Institute (SIPRI) Military Expenditure Database:
https://doi.org/10.55163/CQGC9685

**Major-arms transfer data:**

Information from the Stockholm International Peace Research
Institute (SIPRI) Arms Transfers Database:
https://doi.org/10.55163/SAFC1241

All statistical analyses, calculations, interpretations and
original visualizations were produced by the author.

### Permission to Publish

SIPRI has granted the author conditional authorization to
publish SIPRI-derived analysis and visualizations in a
personal, non-commercial academic and professional portfolio.

This authorization applies to the author acting as a
private individual and is subject to SIPRI's conditions.
SIPRI reserves the right to withdraw authorization.

Commercial use, including use through a business or
sole-trader activity, may require a separate licence.

The original SIPRI databases, downloaded datasets and
database exports are not redistributed through this
repository or the associated portfolio website.

The authorization granted to the author does not constitute
a general licence for third parties to redistribute or
commercialize SIPRI data.

### Geographical Data

Geographical data were obtained from Eurostat GISCO:
https://ec.europa.eu/eurostat/web/gisco

© EuroGeographics for the administrative boundaries.

Reuse of GISCO geographical data remains subject to its
own applicable licence conditions and attribution
requirements.

### Research Code

The Python notebook contains the author's original
analytical code and methodology.

Saved notebook outputs were removed before publication
to avoid redistributing embedded source data.

Users wishing to reproduce the results must obtain the
underlying datasets from their official providers and
comply with the applicable terms and conditions.


## Limitations

The EU sample is modest, geographical proximity is defined in particular ways, and military expenditure and arms deliveries measure different concepts. Association does not establish causation. This repository contains research code, not a policy recommendation or validated forecasting system.
