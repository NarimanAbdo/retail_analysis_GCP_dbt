# 📊 Retail Analysis on GCP with dbt

A scalable and modular retail data pipeline built on **Google Cloud Platform (GCP)** using **dbt** for transformation. This repository ingests, cleans, transforms, and analyzes retail sales data to derive business insights.

├── models/
│   ├── staging/           # raw-to-cleaned transformations
│   ├── marts/             # analytics-ready models
│   └── snapshots/         # snapshot definitions for SCD
├── seeds/                 # static reference data
├── tests/                 # custom SQL/data tests
├── docs/                  # model docs & ERD assets
├── macros/                # re-usable dbt macros
├── profiles.yml.example   # sample dbt profile
├── requirements.txt       # Python deps
└── README.md              # this file

## Table of Contents

- [Overview](#overview)  
- [Architecture](#architecture)  
- [Prerequisites](#prerequisites)  
- [Setup & Installation](#setup--installation)  
- [Usage](#usage)  
  - [Development](#development)  
  - [Production & Deployment](#production--deployment)  
- [Project Structure](#project-structure)  
- [Testing](#testing)  
- [Contributing](#contributing)  
- [License](#license)  
- [Contact](#contact)

---

## Overview

This project provides a complete end-to-end pipeline to analyze retail sales performance, including:

1. **Ingestion**: Raw data loaded into GCP (e.g. Cloud Storage, BigQuery).  
2. **Transformation**: dbt models for cleaning, deduplication, aggregation, and business metrics.  
3. **Analytics**: Pre-built models for sales trends, product performance, cohort analysis, and KPI dashboards.

---

## Architecture


Components:

- **GCS**: raw file storage  
- **BigQuery**: central analytics warehouse  
- **dbt**: SQL-based transformations  
- **Scheduler**: Airflow / Cloud Composer / Cloud Scheduler for orchestration

---

## Prerequisites

- Google Cloud Project with:
  - BigQuery dataset(s)
  - Cloud Storage bucket
- Python 3.8+ & `pip`
- `dbt-core` and `dbt-bigquery` adapters
- (Optional) Airflow or Composer for scheduling

---

## Setup & Installation

1. **Clone the repo**
   ```bash
   git clone https://github.com/NarimanAbdo/retail_analysis_GCP_dbt.git
   cd retail_analysis_GCP_dbt
