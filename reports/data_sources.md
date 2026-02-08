# Data Sources and Attribution

This repository uses publicly available, non-identifiable environmental and population-health datasets. No individual-level or protected health information (PHI) is used.

---

## Air Quality (PM2.5)

**Source:** U.S. Environmental Protection Agency (EPA), Air Quality System (AQS)  
**Dataset:** Daily PM2.5 FRM/FEM Mass (Parameter Code 88101)  
**Use in this project:** County-level PM2.5 exposure summaries (monthly aggregation) for the DMV region.

- EPA AQS overview: https://www.epa.gov/aqs  
- AQS data access (files/API): https://aqs.epa.gov/aqsweb/documents/data_api.html

**Notes:**
- PM2.5 values are measured at regulatory monitoring sites. County-level summaries aggregate across available sites and days.
- Units are as provided by AQS (typically µg/m³).

---

## Meteorology 

**Source:** National Oceanic and Atmospheric Administration (NOAA), National Centers for Environmental Information (NCEI)  
**Dataset:** Integrated Surface Database (ISD)  
**Use in this project:** Optional covariates (temperature, wind, humidity) for exposure–outcome modeling.

- ISD product page: https://www.ncei.noaa.gov/products/land-based-station/integrated-surface-database

---

## Population Health Outcomes (CDC PLACES)

**Source:** Centers for Disease Control and Prevention (CDC), PLACES: Local Data for Better Health  
**Dataset:** PLACES County Data (model-based estimates)  
**Use in this project:** County-level health indicators (e.g., asthma/COPD/cardiovascular prevalence) to evaluate associations with PM₂.₅ exposure.

- CDC PLACES homepage: https://www.cdc.gov/places/  
- PLACES methodology/documentation is linked from the PLACES site.

**Notes:**
- PLACES provides modeled prevalence estimates based on BRFSS and small-area estimation methods; outputs are intended for public health surveillance and planning.
- Analyses in this repository evaluate associations in aggregated data and are not intended as causal or clinical claims.

---

## Provenance within this repository

- Environmental exposure table created in: `notebooks/01_exposure_aggregation.ipynb`  
  Output: `data/processed/pm25_county_monthly_dmv.csv`

If additional datasets are added (e.g., CMS hospitalizations or CDC WONDER mortality), this file should be updated with corresponding citations and links.
This project is intended for educational and research demonstration purposes and does not constitute public health guidance.

