# ETL Pipeline — League A Data

A practical data engineering project built to practise end-to-end ETL pipeline development using the Medallion Architecture (Raw → Stage → Trusted → Delivery) on Databricks.

## Overview

This project simulates a real-world sports data pipeline, ingesting, transforming, and delivering data for analytical use.  
The goal is to showcase enterprise data engineering patterns in a reproducible environment.

## Architecture

1. **RAW Layer** ← Raw JSON data ingested directly from League A API
2. **STAGE Layer** ← JSON parsed to Spark DataFrames, schema enforced
3. **TRUSTED Layer** ← Data cleaned, deduplicated, validated
4. **DELIVERY Layer** ← Final curated datasets for BI/dashboard use

Each layer stored as **Delta Lake tables** with ACID transactions.

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

Pedro Ribeiro — Data Engineer & BI Developer based in Sydney, Australia  
[LinkedIn](https://www.linkedin.com/in/pedroribeiroit/) · [GitHub](https://github.com/Mousinho)
