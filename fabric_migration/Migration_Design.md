# Snowflake to Microsoft Fabric Sales Migration

## 1. Project Overview

This project demonstrates the migration of a Sales Analytics workload from Snowflake to Microsoft Fabric.

The original production architecture is considered as:

Snowflake → Microsoft Fabric → Power BI

For this hands-on POC, GitHub CSV files are used to simulate the Snowflake source because a Snowflake environment is not available.

---

## 2. Source System

### Production Source

- Source Platform: Snowflake
- Source Table: FACT_SALES
- Source Type: Relational Data Warehouse

### POC Source

- Source Platform: GitHub
- Source File: fact_sales.csv
- Format: CSV

GitHub is used only as a source simulation for this hands-on implementation.

---

## 3. Target Platform

### Microsoft Fabric

The target architecture uses:

- Fabric Data Factory
- Fabric Lakehouse
- PySpark
- Delta Lake
- OneLake
- Power BI Semantic Model
- Power BI Report

---

## 4. Migration Architecture

```text
                    SOURCE
                  Snowflake
                 FACT_SALES
                     |
                     |
              Migration Extract
                     |
                     v
          Microsoft Fabric Data Factory
                     |
                 Copy Activity
                     |
                     v
          Fabric Lakehouse
          LH_Sales_Migration
                     |
              +------+------+
              |             |
              v             v
        fact_sales_raw   PySpark
                            |
                            v
                       fact_sales
                            |
                            v
                  Direct Lake Semantic
                       Model
                            |
                            v
                       Power BI



