# Missouri Water Information System – ETL Pipeline

## Overview

This project presents a real-time data engineering system developed as part of a published research paper.

The system integrates hydrologic data from multiple external APIs (NOAA, USGS) and processes it through an automated ETL pipeline for analytics and visualization.

📄 Paper: [http://dx.doi.org/10.2139/ssrn.5277101]

---

## System Architecture

![Architecture](architecture.png)

The platform consists of:

* Data ingestion from external APIs
* Backend processing (ETL pipeline)
* Relational database storage
* API layer for data serving

---

## ETL Pipeline

![Pipeline](pipeline.png)

### Ingestion

* USGS API → real-time sensor data (15-minute updates)
* NOAA API → forecast data (hourly updates)
* External rainfall servers

### Transformation

* Timestamp normalization (UTC standardization)
* Schema alignment across APIs
* Data cleaning and validation

### Storage

* MySQL relational database
* Normalized schema (3NF)
* Time-series data with composite keys

### Serving

* Flask API
* JSON responses for frontend visualization

---

## Data Quality & Reliability

* Validation for missing or invalid values
* Retry logic for API failures
* Error logging
* Deduplication using sensor ID + timestamp
* Redis caching for performance

---

## Pipeline Scheduling

* Cron jobs:

  * Observations → every 15 minutes
  * Forecasts → hourly
* Automated cleanup and cache management

---

## Technologies

* Python
* Flask
* MySQL
* Redis
* Cron Jobs

---

## Key Data Engineering Concepts

* ETL pipeline design
* Multi-source data integration
* Data validation and cleaning
* Time-series processing
* Pipeline automation
* Scalable system architecture

---

## Note

This repository focuses on system architecture and data pipeline design derived from a production-scale research system.

I’d be happy to walk through implementation details and how this could be extended using PySpark and Databricks.
