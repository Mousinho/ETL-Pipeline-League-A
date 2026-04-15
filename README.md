# ETL Pipeline — League A Data

A practical data engineering project built to practise end-to-end ETL pipeline development using the Medallion Architecture (Raw → Stage → Trusted → Delivery) on Databricks.

## Overview

This project simulates a real-world sports data pipeline, ingesting, transforming, and delivering data for analytical use.  
The goal is to showcase enterprise data engineering patterns in a reproducible environment.

## Architecture
API Source (League A)
↓
RAW Layer ← Raw JSON ingested as-is
↓
STAGE Layer ← Schema enforced DataFrames
↓
TRUSTED Layer ← Cleaned & validated data
↓
DELIVERY Layer ← BI-ready datasets

Each layer is stored as a Delta Lake table, enabling schema enforcement, version control, and ACID transactions — a key advantage in modern data lake design.

## Tech Stack

| Tool | Purpose |
|------|---------|
| Databricks | Unified analytics and notebook environment |
| Apache Spark / PySpark | Distributed data processing |
| Delta Lake | Transactional and versioned storage layer |
| Python | Data extraction and transformation |
| REST API | External data source for ingestion |

## What I Practised

- Consuming structured sports data from a REST API.
- Implementing the Medallion Architecture for incremental, reliable data transformation.
- Using Delta Lake for versioning and clean data management.
- Applying schema enforcement, validation, and deduplication logic.
- Using Databricks notebooks for orchestration and pipeline modularization.

## How to Run

1. Clone this repository to your local environment or Databricks workspace.
2. Import each notebook into Databricks (`File → Import`).
3. Execute the notebooks sequentially: **Raw → Stage → Trusted → Delivery**.
4. A free Databricks Community Edition account is sufficient to run this workflow.

## Author

Pedro Ribeiro — Data Analyst & BI Developer based in Sydney, Australia  
[LinkedIn](https://www.linkedin.com/in/pedroribeiroit/) · [GitHub](https://github.com/Mousinho)
