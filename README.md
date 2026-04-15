# ETL Pipeline — League A Data

A practical data engineering project built to practise end-to-end ETL pipeline development using the Medallion Architecture (Raw → Stage → Trusted → Delivery) on Databricks.

## Overview

This project simulates a real-world sports data pipeline, ingesting, transforming, and delivering data for analytical use.  
The goal is to showcase enterprise data engineering patterns in a reproducible environment.

## Architecture

```text
API Source
   |
   v
RAW Layer
   |
   v
STAGE Layer
   |
   v
TRUSTED Layer
   |
   v
DELIVERY Layer
```

## Tech Stack

| Tool | Purpose |
|------|---------|
| Databricks | Notebook environment |
| Apache Spark / PySpark | Data processing |
| Delta Lake | Reliable storage |
| Python | Extraction and transformation |
| REST API | Data source |

## What I Practised

- Consuming data from a REST API.
- Applying the Medallion Architecture.
- Using Delta Lake for versioned storage.
- Enforcing schema and validating data.
- Building the pipeline in Databricks notebooks.

## How to Run

1. Clone the repository.
2. Import the notebooks into Databricks.
3. Run them in order: Raw → Stage → Trusted → Delivery.
4. Use Databricks Community Edition if needed.

## Author

Pedro Ribeiro — Data Analyst & BI Developer based in Sydney, Australia  
[LinkedIn](https://www.linkedin.com/in/pedroribeiroit/) · [GitHub](https://github.com/Mousinho)
