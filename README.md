# Air Quality Assessment for Health Modeling (DMV)

## Overview
This project investigates how short-term exposure to fine particulate matter (PM2.5) relates to population-level health outcomes in the Washington, DC–Baltimore (DMV) region. Building on an exposure modeling pipeline developed in Project 1, I aggregate environmental exposures and evaluate associations with county-level health indicators using interpretable statistical models and machine-learning baselines.

The goal is not causal attribution, but to demonstrate rigorous, transparent applied ML practices for environmental health data, including time-aware aggregation, uncertainty-aware modeling, and clear interpretation of results.

---

## Scientific Questions
1. Do higher PM2.5 exposure levels associate with higher respiratory or cardiovascular health burden at the county level?
2. Do lagged exposure windows (e.g., recent multi-day or monthly averages) improve explanatory power?
3. Which features (PM2.5 exposure, meteorology, seasonality) dominate model behavior, and with what uncertainty?

---

## Data Sources
- **Air Quality:** EPA Air Quality System (AQS) PM2.5 (daily, site-level)
- **Meteorology:** NOAA ISD / surface meteorological observations
- **Health Outcomes:** CDC PLACES (county-level prevalence indicators)

All datasets are publicly available. No individual-level or protected health information is used.

---

## Methods
- **Exposure aggregation:** PM2.5 aggregated to county-level time series (monthly or annual), with lagged exposure windows.
- **Baseline statistics:** Generalized Linear Models (GLM) using `statsmodels`, with robust standard errors and confidence intervals.
- **ML baselines:** Regularized regression and tree-based models (Random Forest; optional gradient-boosted trees).
- **Uncertainty handling:** Confidence intervals for effect estimates; bootstrap uncertainty for model metrics.
- **Exploratory analysis:** Dimensionality reduction and clustering to identify counties with similar exposure profiles.

---

## Repository Structure
## Project Structure

- `data/`: raw and processed datasets  
- `notebooks/`: exploratory analysis and modeling notebooks  
- `src/`: data ingestion, aggregation, and preprocessing scripts  
- `figures/`: saved plots and figures  
- `reports/`: short summaries, notes, and documentation  

All data used in this project are publicly available from the U.S. EPA, NOAA, and CDC; see `reports/data_sources.md` for full attribution and provenance details.
Health outcome data are sourced from the CDC PLACES project; see reports/data_sources.md for full attribution.

## Notes on Interpretation
Results reflect associations in aggregated, population-level data. They are intended for methodological demonstration and hypothesis generation, not causal inference or clinical decision-making.

