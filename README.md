# Daiichi-Life-Demo

A public portfolio/demo project that demonstrates an end-to-end **Azure + Microsoft Fabric + Power BI** analytics implementation for a synthetic life-insurance use case.

> **Disclaimer:** This repository is an independent technical demonstration created using synthetic data. It is **not an official Daiichi Life project**, does not contain Daiichi Life data, and is not affiliated with or endorsed by Daiichi Life.

## Project Goal

The objective is to demonstrate how a modern BI solution can be designed across:

- Azure SQL
- Azure Data Factory
- ADLS Gen2
- Microsoft Fabric
- OneLake
- Lakehouse
- Notebooks
- Data Science / ML
- Direct Lake Semantic Model
- Power BI
- DEV → TEST → PROD deployment

The demo uses a synthetic life-insurance scenario covering policy performance, customer analytics, distribution performance, geography, and lead-conversion prediction.

## High-Level Flow

```text
Azure SQL
   ↓
Azure Data Factory
   ↓
ADLS Gen2
   ↓
OneLake Shortcut
   ↓
Fabric Lakehouse
   ↓
Silver / Gold Delta Tables
   ↓
Fabric Data Science Notebook
   ↓
Lead Conversion Prediction
   ↓
Direct Lake Semantic Model
   ↓
Power BI
   ↓
DEV → TEST → PROD
```

For the detailed architecture and implementation flow, see:

- [`Flow.md`](./Flow.md)

## Repository Structure

```text
Daiichi-Life-Demo/
│
├── README.md
├── Flow.md
│
└── PBIP/
    └── Power BI Project files
```

### `README.md`

Provides a short overview of the project, architecture, scope, and repository structure.

### `Flow.md`

Contains the detailed end-to-end architecture and implementation steps covering:

- Azure source and ingestion
- ADLS landing
- Fabric integration
- Lakehouse design
- Silver / Gold transformation
- Machine-learning scoring
- Semantic model
- Power BI
- DEV / TEST / PROD deployment

### `PBIP/`

Contains the Power BI Project source files used for the demo.

## Demo Business Areas

The Power BI solution is designed to demonstrate:

- Executive insurance KPIs
- Policy and product performance
- Customer segmentation
- Geographic analysis
- Distribution / agent performance
- Renewal and lapse analysis
- Lead funnel analysis
- AI/ML-based lead conversion propensity

## Data Science Use Case

A Fabric notebook is used to demonstrate a lead-conversion prediction workflow.

The model scores open leads and produces outputs such as:

- Conversion probability
- Predicted conversion flag
- Propensity band
- Model version
- Scoring timestamp

The scored output can then be consumed by Power BI for prioritization and sales analysis.

## Important Notes

- All data used in this project is synthetic.
- No real customer, policy, employee, or company-confidential data is included.
- No production credentials, secrets, tokens, connection strings, tenant IDs, or private endpoints should be committed to this repository.
- Architecture shown here is a demonstration pattern and can be adapted based on the target organization's real environment, security model, governance requirements, and data volumes.

## Technologies

- Microsoft Azure
- Azure SQL
- Azure Data Factory
- ADLS Gen2
- Microsoft Fabric
- OneLake
- Fabric Lakehouse
- Fabric Notebook
- MLflow
- Power BI
- DAX
- Power Query / M
- Direct Lake
- PBIP

## Author

**Manikandan Baskar**

Senior BI / Power BI / Data & Automation Professional
