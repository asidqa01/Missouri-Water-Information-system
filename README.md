# Missouri-Water-Information-system
## Water Data ETL Pipeline (Missouri Water Information System)

## Overview

This project demonstrates the design of a real-world data pipeline that integrates multiple environmental data sources including NOAA, USGS, and rainfall servers.

The system was developed as part of a published research project and focuses on ETL pipeline design, data integration, and time-series processing.

---

## What This Project Shows

* Multi-source data ingestion (APIs + external datasets)
* Data cleaning and transformation (timestamps, missing values)
* Schema normalization across heterogeneous data
* Scheduled data pipelines (15-minute updates)
* API-based data serving (Flask)
* Geospatial visualization support

---

## Data Sources

* NOAA API (weather and rainfall)
* USGS API (streamflow and sensor data)
* Rainfall processing server (map overlays)

---

## ETL Pipeline Design

**Ingestion**

* Fetch data from APIs and external sources
* Handle JSON and CSV formats

**Transformation**

* Convert timestamps (GMT → CST)
* Clean missing and inconsistent values
* Normalize schema

**Output**

* Store structured data in database
* Serve via API for frontend visualization

---

## Data Quality Considerations

* Missing sensor values
* Timestamp inconsistencies
* Duplicate records from multiple sources
* Data normalization across APIs

---

## Research Paper

This work is based on my published research:

[Add your DOI link here]

---

## Note

This repository focuses on system design, pipeline architecture, and data engineering concepts rather than full production code.

I’d be happy to walk through implementation details, tradeoffs, and scaling considerations in discussion.
