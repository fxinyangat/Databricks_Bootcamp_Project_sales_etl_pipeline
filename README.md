# Sales ETL Pipeline — Databricks Lakehouse Project

## Overview
This project is an end-to-end **Sales ETL & Analytics Pipeline** built on **Databricks Serverless**, using **PySpark**, **Delta Lake**, and **Lakeflow Declarative Pipelines**. It automates the ingestion, cleaning, transformation, and aggregation of raw sales and customer data—progressing from **Bronze → Silver → Gold** managed layers.

The final deliverables include:
- A production-ready ETL pipeline using Databricks & PySpark  
- A Gold-level aggregated dataset (`gold_aggregates`)  
- A Databricks SQL dashboard visualizing key sales KPIs  

This repository reflects the capstone work completed as part of the  
**“Complete Databricks & PySpark Bootcamp: Zero to Hero”**, where the final project required building a complete data engineering pipeline with a visualization dashboard.

---

## Purpose
The goal of this project is to demonstrate the design and implementation of a scalable, governed, and automated ETL workflow that produces clean, enriched, and analytics-ready datasets.  

This pipeline enables:
- Reliable sales and customer analytics  
- Faster KPIs and reporting  
- Improved customer segmentation  
- Data-driven decision-making powered by curated Gold data  

It showcases modern Lakehouse engineering practices using PySpark and Delta Lake.

---

## Architecture

### **Medallion Architecture**
<img width="1099" height="885" alt="image" src="https://github.com/user-attachments/assets/3c46f1ec-ffbf-43cf-947d-40fe814f80ea" />


#### **1. Bronze Layer — Raw Ingestion**
- Ingests raw sales and customer datasets  
- Uses Auto Loader and serverless compute for scalable ingestion  
- Stores raw data as Delta for reliability and schema evolution  

#### **2. Silver Layer — Cleaning & Transformation**
- Handles missing, inconsistent, and malformed fields  
- Applies normalization and business logic  
- Produces cleaned tables such as `silver_orders_py`  
- Enriches data with customer details & standardized formats  

#### **3. Gold Layer — Aggregations & Analytics**
- Joins customer + sales tables  
- Computes revenue metrics, sales KPIs, and time-based trends  
- Stores analytics-ready results in `gold_aggregates`  
- Serves dashboards, BI tools, and downstream models  

### **Pipeline Orchestration**
- Implemented using **Lakeflow Declarative Pipelines**  
- Uses decorators, expectations, and modular pipeline design  
- Orchestrated on **Databricks Serverless** for efficient autoscaling  
- Integrated with **Unity Catalog** for governance, permissions, and schema control  

---

## Dashboard
A Databricks SQL dashboard is built on the `gold_aggregates` table, providing:

- **Total Sales & Revenue Trends**  
- **Top Performing Products**  
- **Customer Segmentation Insights**  
- **Monthly / Quarterly Performance Metrics**  
- **Operational KPIs**

<img width="1549" height="900" alt="image" src="https://github.com/user-attachments/assets/029bd0b1-cf8e-45d0-92a6-1f1f3cbc9e8d" />


This dashboard enables stakeholders to quickly view clean, trusted insights derived from the curated Gold layer.

---

## Technologies Used
- **Databricks Lakehouse Platform**  
- **PySpark / Spark DataFrames**  
- **Delta Lake**  
- **Unity Catalog**  
- **Lakeflow Declarative Pipelines**  
- **Databricks Serverless Compute**  
- **Auto Loader**  
- **Databricks SQL Dashboards**  
- **Medallion Architecture (Bronze, Silver, Gold)**  

---

## Skills Demonstrated
- Building end-to-end Databricks ETL pipelines using PySpark  
- Implementing the Medallion Architecture with Delta Lake  
- Data ingestion, cleaning, standardization, and enrichment  
- Aggregations, KPI computation, and analytics modeling  
- Writing declarative pipelines with expectations and modular logic  
- Leveraging serverless compute for scalable workloads  
- Dashboard development in Databricks SQL  
- Applying Unity Catalog for secure governance and lineage  

---

## Business Impact
- **Reliable Sales Analytics**: Gold tables deliver fast, accurate insights for performance tracking and forecasting.  
- **Data-Driven Decisions**: Clean, enriched data enables improved targeting, product optimization, and strategic planning.  
- **Operational Efficiency**: Automated pipelines reduce manual effort and ensure continuous data freshness.  
- **Governance & Compliance**: Unity Catalog enforces secure access, auditability, and schema governance.

---

If you want, I can also generate:
- A **project diagram (Mermaid)**  
- A **“How to Run This Project”** section  
- A **GitHub-optimized portfolio version**  
