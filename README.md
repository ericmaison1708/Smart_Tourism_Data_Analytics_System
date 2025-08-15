# Smart Tourism Data Analytics System

A smart data analytics platform that collects, processes, and visualizes tourism data from multiple sources (Tripadvisor, Booking, internal datasets) — powered by Python, Oracle Data Integrator (ODI), MySQL/Oracle Database, and BI tools (Power BI/Tableau).

## Table of Contents

- [Overview](#overview)
- [Architecture](#architecture)
- [System-Setup](#system-setup)
- [Results](#results)

## Overview

The system is designed to:

1. **Extract** tourism data (hotels, restaurants, attractions) from multiple sources using web crawling and APIs.
2. **Transform** raw data (cleaning, deduplication, schema normalization, missing value handling) with Python or ODI.
3. **Load** processed data into a centralized **Data Warehouse** (MySQL/Oracle) using Star Schema.
4. Provide **interactive dashboards** in Power BI/Tableau to analyze and visualize tourism trends, prices, ratings, and seasonal patterns.

---

## Architecture
```mermaid
flowchart LR
  A[Data Sources: Tripadvisor, Booking, Internal CSV/API] --> B[Data Crawling: Python (Selenium, BeautifulSoup)]
  B --> C[Raw Storage: CSV/Cloud Storage]
  C --> D[ETL Pipeline: Python Scripts / Oracle Data Integrator]
  D --> E[(Data Warehouse: MySQL/Oracle)]
  E --> F[Visualization: Power BI/Tableau]
