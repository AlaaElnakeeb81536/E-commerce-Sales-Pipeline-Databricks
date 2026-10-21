#  E-Commerce Sales Data Pipeline

![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=for-the-badge&logo=databricks&logoColor=white)
![PySpark](https://img.shields.io/badge/PySpark-E25A1C?style=for-the-badge&logo=apachespark&logoColor=white)
![Delta Lake](https://img.shields.io/badge/Delta%20Lake-003366?style=for-the-badge&logo=delta&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)

##  Project Overview

An end-to-end ELT data pipeline built using **Databricks Community Edition, PySpark, and Delta Lake** to process over 30,000 e-commerce sales records.
The project follows the **Medallion Architecture (Bronze → Silver → Gold)** to transform raw data into clean, structured, and analytics-ready datasets. The workflow is orchestrated using Databricks Jobs, with task dependencies and automated email notifications.

## 🏗️Architecture

```
Kaggle CSV
    ↓
[Bronze Layer]  →  Raw data ingestion → Delta Table
    ↓
[Silver Layer]  →  Cleaning & Transformation → Delta Table
    ↓
[Gold Layer]    →  Aggregations & KPIs → 4 Delta Tables
    ↓
[Dashboard]     →  4 Charts in Databricks SQL
```
## 🥉 Bronze Layer – Raw Data Ingestion

The Bronze layer stores the raw data ingested from the source CSV file into Delta tables in its original format, preserving the source data for further processing.

## 🥈 Silver Layer – Data Cleaning & Transformation

The Silver layer processes the raw Bronze data using PySpark by handling missing values, removing duplicates, correcting data types, and preparing clean, structured data for analytics. The transformed data is stored in Delta tables.

##  Gold Layer Analytics

The Gold layer provides four datasets for analyzing:

| Analytical Table | Purpose |
|---|---|
| Monthly Revenue | Track revenue trends over time |
| Product Sales | Analyze product-level sales performance |
| City Performance | Compare sales performance across cities |
| Hourly Sales | Identify sales patterns by hour |

## Tech Stack

| Technology | Purpose |
|---|---|
| **Databricks Community Edition** | Development and execution environment |
| **Apache PySpark** | Data processing and transformation |
| **Delta Lake** | Storage and management of processed data |
| **Python** | Pipeline development |
| **Databricks Jobs** | Workflow orchestration and job scheduling |
| **Databricks SQL** | Data querying and dashboard visualization |

##  Key Learnings

- Building multi-layer data pipelines using the Medallion Architecture.
- Processing and transforming data with PySpark.
- Working with Delta Lake tables.
- Creating analytical datasets for business intelligence.
- Orchestrating dependent pipeline tasks in Databricks.

