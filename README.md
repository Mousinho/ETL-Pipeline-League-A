ETL Pipeline — League A Data
A practical data engineering project designed to build an end-to-end ETL pipeline using modern tools and the Medallion Architecture (Raw → Stage → Trusted → Delivery) on Databricks, focused on ingesting, transforming, and delivering sports data for analytical use.

Overview
This project simulates a real-world scenario of ingesting and processing sports data — specifically data from “League A,” which includes teams, players, matches, and performance metrics.
The goal is to showcase enterprise-grade data engineering techniques in a reproducible environment while establishing a clean data flow from unstructured ingestion to curated analytical outputs.

Data is collected from the League A API, transformed through structured layers, and stored as Delta Lake tables for reliability, versioning, and scalability.

Architecture
API Source (League A)
│
▼
┌───────────────┐
│ RAW Layer │ ← Raw JSON data ingested directly from the API
└───────┬────────┘
│
▼
┌────────────────┐
│ STAGE Layer │ ← JSON parsed to Spark DataFrames, schema defined
└───────┬────────┘
│
▼
┌─────────────────┐
│ TRUSTED Layer │ ← Data cleaned, deduplicated, and validated
└───────┬────────┘
│
▼
┌───────────────────┐
│ DELIVERY Layer │ ← Final curated datasets ready for BI or dashboard use
└───────────────────┘

Each layer is stored as a Delta Lake table, enabling schema enforcement, version control, and ACID transactions — a key advantage in modern data lake design.

Tech Stack
Tool	Purpose
Databricks	Unified analytics and notebook environment
Apache Spark / PySpark	Distributed data processing
Delta Lake	Transactional and versioned storage layer
Python	Data extraction and transformation
REST API (League A)	External data source for ingestion
Project Structure
text
ETL_League_A/
│
├── Raw_LeagueA.ipynb         # Layer 1: Extract data → Raw Delta table  
├── Stage_LeagueA.ipynb       # Layer 2: Enforce schema → Stage Delta table  
├── Trusted_LeagueA.ipynb     # Layer 3: Clean data → Trusted Delta table  
├── Delivery_LeagueA.ipynb    # Layer 4: Curate dataset → Delivery Delta table  
└── README.md  
What I Practised
Consuming structured sports data from a REST API.

Implementing the Medallion Architecture for incremental, reliable data transformation.

Using Delta Lake for versioning and clean data management.

Applying schema enforcement, validation, and deduplication logic.

Using Databricks notebooks for orchestration and pipeline modularization.

How to Run
Clone this repository to your local environment or Databricks workspace.

Import each notebook into Databricks (File → Import).

Execute the notebooks sequentially: Raw → Stage → Trusted → Delivery.

A free Databricks Community Edition account is sufficient to run this workflow.

Author
Pedro Ribeiro — Data Analyst & BI Developer based in Sydney, Australia
LinkedIn · GitHub
