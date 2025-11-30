# LongevityAnalytics

**Life‑table & survival‑analysis framework for actuarial analytics**

## Overview
Insurance and pension funds rely on accurate mortality estimates. This project builds a modern analytics framework that transforms raw demographic and claims data into actuarial life tables and survival‑analysis models. It demonstrates data engineering, statistical modelling and data‑visualisation skills.

## Business Problem
A fictional life insurer needs to estimate mortality rates and life expectancy for pricing annuities and life‑insurance products. Existing spreadsheets are error‑prone and cannot handle censored survival data. The organisation requires a reproducible system that cleans data, constructs life tables, applies Kaplan–Meier and Cox models with censoring, and communicates results through dashboards and reports.

## Features
- **Data cleaning and transformation**: Python & SQL scripts remove duplicates, fix structural errors, handle missing dates and outliers.
- **Life‑table construction**: Compute age intervals, survivors (lx), deaths (dx), death probability (qx), survival probability (px) and life expectancy (ex).
- **Survival models**: Implement Kaplan–Meier and Cox proportional hazards models to estimate survival functions and hazard rates.
- **Monte‑Carlo simulation**: Generate confidence bands around life‑expectancy estimates and evaluate variability.
- **Dashboards and reports**: Interactive Power BI/Tableau dashboard visualises survival curves, hazard rates and demographic filters. An executive PDF summarises actuarial insights for non‑technical stakeholders.
- **Reproducible workflow**: Version‑controlled notebooks, Python modules, SQL scripts and Excel models allow easy replication and extension.

## Repository Structure
```
longevityanalytics/
├── data/          # raw & processed mortality/claims data
├── src/           # Python modules for cleaning, life‑table construction & simulations
├── notebooks/     # Jupyter notebooks demonstrating survival analysis & modelling
├── dashboards/    # Power BI or Tableau dashboards (.pbix or .twb)
├── docs/          # executive summary PDF, actuarial assumptions & diagrams
├── requirements.txt # Python dependencies
└── README.md      # project overview, instructions & methodology
```

## Getting Started
1. **Clone the repository**  
   ```bash
   git clone https://github.com/<your-username>/longevityanalytics.git
   cd longevityanalytics
   ```
2. **Install dependencies**  
   It’s recommended to use a virtual environment:  
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # On Windows use `.venv\\Scripts\\activate`
   pip install -r requirements.txt
   ```
3. **Set up the data**  
   - Place raw demographic and claims data in the `data` folder.  
   - Run the SQL scripts in `src/` to create the database and load raw data.

4. **Run the analysis**  
   - Explore the notebooks in `notebooks/` to clean data, build life tables, fit survival models and run simulations.  
   - Use the Python modules in `src/` for reusable functions and classes.  
   - Open the Power BI/Tableau file in `dashboards/` to interact with the visualisations.

5. **Review the reports**  
   - The `docs/` folder contains an executive summary PDF and supporting documentation explaining assumptions, methodology and insights.

## Deliverables
This repository produces multiple artefacts:
- Cleaned mortality dataset and actuarial life table.
- Python modules and Jupyter notebooks implementing data cleaning, life‑table construction, Kaplan–Meier and Cox models, and Monte‑Carlo simulations.
- SQL scripts to ingest raw data into SQLite/PostgreSQL.
- Excel workbook calculating life expectancy and premium factors.
- Interactive Power BI/Tableau dashboard.
- Executive summary PDF and supporting documentation.

## Extensions
Potential enhancements include:
- Implement competing‑risks or frailty models for multiple causes of death.
- Use Bayesian survival models (e.g., PyMC) and compare with frequentist results.
- Deploy the life‑table computation as a REST API and integrate continuous integration tests.

## License
Add your preferred license here (e.g., MIT).
