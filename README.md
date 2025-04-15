# 🏢 Azure Data Engineering Project – Customer, Product & Sales Analytics

This project showcases a complete end-to-end data engineering solution using Azure services, focused on analyzing **customer behavior**, **product performance**, and **sales trends**. It demonstrates how to build scalable data pipelines and warehouses using Azure Data Factory, Databricks (Apache Spark), Azure Synapse Analytics, and Power BI.

---
 
## 📊 Business Use Case

A retail company wants to:
- Track **customer engagement** and regional growth
- Analyze **product categories**, pricing, and inventory trends
- Monitor **sales performance** across channels and time
- Enable near real-time reporting for decision-makers

---

## 📖 Introduction

This project demonstrates how to design and implement an end-to-end data pipeline using Azure services. It extracts data from an API, processes and transforms it using Databricks and Apache Spark, and finally loads it into Azure Synapse Analytics for analysis and visualization via Power BI.

---

## 🏗️ Data Architecture

We follow the **Medallion Architecture** for data organization:

- **Bronze Layer**: Raw data ingestion
- **Silver Layer**: Cleansed and transformed data using PySpark
- **Gold Layer**: Aggregated and modeled data for reporting


---

## 🧠 Key Features

- Ingest customer, product, and sales data using **Azure Data Factory**
- Transform large datasets with **Apache Spark** in **Databricks**
- Build a data warehouse in **Azure Synapse Analytics**
- Visualize KPIs in **Power BI Dashboards**:
  - Customer acquisition trends
  - Top-performing products
  - Regional sales breakdown
  - Year-over-year sales growth
 
---

## 🔁 Pipeline Flow Overview

1. **Ingest**: Data pulled from REST APIs (or CSV dumps)
2. **Store**: Raw data stored in Azure Data Lake (Bronze)
3. **Transform**: Using PySpark in Databricks (Silver)
4. **Warehouse**: Cleaned and modeled data loaded into Synapse (Gold)
5. **Visualize**: Connected to Power BI for stakeholder insights

---

## 📚 Project Modules

- **Data Factory Pipelines** – Data ingestion orchestration
- **Databricks Notebooks** – Cleaning and joining customer/product/sales data
- **Spark Jobs** – ETL logic for building dimension and fact tables
- **Synapse SQL Scripts** – Creating external tables and views
- **Power BI Reports** – Dashboards using gold layer tables

---


## 📡 Data Understanding (API)

We ingest real-time or scheduled data from an open API, such as a weather, finance, or e-commerce dataset.  
The raw JSON/CSV data is stored in the Bronze layer of Azure Data Lake Gen2.

---

## 🔁 Data Ingestion (Bronze Layer)

- Data is pulled using **Azure Data Factory Pipelines**
- Stored securely in **Azure Data Lake Gen2**
- Implements parameterized pipelines and dynamic datasets

---

## ⚙️ Creating Azure Resources

Azure services used:
- Azure Data Factory
- Azure Storage (Data Lake Gen2)
- Azure Databricks
- Azure Synapse Analytics
- Power BI (Desktop/Service)

---

## 🏭 Azure Data Factory Overview

- ADF is used to orchestrate data movement from API → Blob Storage
- Supports triggers, monitoring, and reusable linked services

---

## 💾 Azure Data Lake Gen2

- Secure and scalable data storage for all ingestion layers
- Supports hierarchical namespace for better folder management

---

## 🔄 ETL Pipelines with Azure Data Factory

- Data ingestion from REST APIs or on-prem sources
- Dynamic pipelines with ForEach, Lookup, Web, and Copy activities
- Logs pipeline run status and failure reasons

---

## 📈 Real-Time Scenarios with ADF

- Trigger data every 1 hour/day using event-based or scheduled triggers
- Handle schema evolution and null values
- Integrate REST API pagination handling in pipeline

---

## ⚡ Azure Databricks Resource

- Set up Databricks using ADF or Azure Portal
- Use a notebook-based approach for transformations

---

## 🔥 Databricks Cluster & Overview

- Configure a standard or autoscaling cluster
- Attach notebooks for transformations
- Schedule jobs using Databricks Jobs or via ADF

---

## 🔐 Service Principal

- Register Azure AD App for secure access between ADF, Databricks, and Storage
- Assign appropriate roles (Storage Blob Data Contributor, etc.)

---

## 🧼 Data Transformation with Databricks

- Read data from Bronze layer
- Clean, normalize, and flatten JSON
- Handle missing values and inconsistent formats

---

## 💡 Apache Spark (Silver Layer)

- Use PySpark to filter, deduplicate, join, and aggregate
- Store cleaned data back in Data Lake as Parquet or Delta format

---

## 🐍 PySpark 

This section includes beginner-to-intermediate PySpark examples:
- DataFrame creation
- Joins, aggregations
- UDFs
- Partitioning and caching

---

## 📊 Big Data Analytics with PySpark

- Perform large-scale joins and aggregations
- Analyze user behavior, trends, and anomalies
- Use `window functions` for time-based analytics

---

## 🏛️ Azure Synapse Analytics (Gold Layer)

- Load curated data from Silver layer into Synapse
- Use PolyBase or COPY statement for ingestion
- Build optimized star/snowflake schema for BI reporting

---

## 🔍 OPENROWSET() Function

- Query data directly from Azure Storage without loading into Synapse tables
- Great for ad-hoc analytics

