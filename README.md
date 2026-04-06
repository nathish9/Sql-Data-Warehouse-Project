# Sql-Data-Warehouse-Project
Building a modern data warehouse with SQL Server,including ETL processes ,data modeling and analytics
## 🚀 Overview

This project demonstrates how to build a modern data warehouse using SQL Server, focusing on:

ETL (Extract, Transform, Load) processes
Data modeling (Star/Snowflake schema)
Data cleaning and transformation
Analytical reporting

The architecture follows a Medallion Architecture approach:
👉 Bronze → Silver → Gold

## 🏗️ Architecture
### 🥉 Bronze Layer (Raw Data)
Stores raw data as-is from source systems
No transformations applied
Acts as a data lake / staging layer

Key Features:

Data ingestion from multiple sources (CSV, APIs, DBs)
Maintains historical raw data
Minimal validation

Example Tables:

bronze_customers_raw
bronze_orders_raw
bronze_products_raw
### 🥈 Silver Layer (Cleaned & Transformed Data)
Data is cleaned, standardized, and validated
Handles missing values, duplicates, and inconsistencies
Prepares data for analytics

Key Features:

Data cleansing (NULL handling, type conversion)
Deduplication
Business rule application

Example Tables:

silver_customers
silver_orders
silver_products
### 🥇 Gold Layer (Business-Ready Data)
Aggregated and modeled for analytics and reporting
Designed using fact and dimension tables

Key Features:

Star schema design
Optimized for queries and dashboards
Supports BI tools (Power BI, Tableau)

Example Tables:

fact_sales
dim_customers
dim_products
dim_date
## 🔄 ETL Process
1. Extract
Load data from source systems into Bronze layer
Tools: SQL Server Integration Services (SSIS) / BULK INSERT
2. Transform
Clean and standardize data in Silver layer
Apply business rules
3. Load
Aggregate and model data into Gold layer
Prepare for analytics
## 🧱 Data Modeling
Star Schema used in Gold layer:
Fact table: transactional data (e.g., sales)
Dimension tables: descriptive attributes (customer, product, date)
🛠️ Tech Stack
Database: SQL Server
ETL: T-SQL / SSIS
Modeling: Star Schema
Analytics: Power BI / Tableau
