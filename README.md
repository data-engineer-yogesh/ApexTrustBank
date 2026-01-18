# 🏦 ApexTrust Bank – Banking Lakehouse Project

## Overview

This project demonstrates a **real-world Banking Data Lakehouse** implementation using **Databricks, Apache Spark, and Delta Lake**. It is designed to showcase **hands-on data engineering skills**, **architecture decision-making**, and **exam-aligned best practices**.

The project follows the **Bronze–Silver–Gold** data modeling pattern and focuses on **ACID transactions, auditability, CDC handling, and BI-ready analytics**, which are critical in regulated domains like banking.

---

## 🎯 Project Goals

* Build a **Lakehouse architecture** on cloud-style object storage
* Practice **Delta Lake operations** (UPDATE, DELETE, MERGE, Time Travel)
* Apply **data quality and validation rules**
* Create **BI-ready analytical tables**
* Demonstrate **interview-ready, job-relevant skills**

---

## 🧱 Architecture

```
Raw Files (CSV)
      ↓
Bronze Layer (Raw Delta – Audit)
      ↓
Silver Layer (Validated Delta)
      ↓
Gold Layer (Analytics Delta)
```

**Why Lakehouse?**

* Supports **structured & semi-structured data**
* Enables **ACID transactions on data lakes**
* Allows **BI, analytics, and ML on the same data**
* Reduces system complexity and data duplication

---

## 🗂️ Git Repository Structure (Exam + Real Project Ready)

```
apextrust-bank-lakehouse/
│
├── README.md
│
├── data/
│   ├── raw/
│   │   ├── customers.csv
│   │   ├── accounts.csv
│   │   ├── transactions.csv
│   │   ├── branches.csv
│   │   └── cdc_customers.csv
│
├── unity-catalog/
│   └── create_catalog_and_schemas.sql
│
├── notebooks/
│   ├── 01_bronze_ingestion/
│   │   └── bronze_ingestion.ipynb
│   │
│   ├── 02_silver_processing/
│   │   └── silver_processing.ipynb
│   │
│   └── 03_gold_analytics/
│       └── gold_analytics.ipynb
│
├── sql/
│   ├── merge_operations.sql
│   ├── time_travel_queries.sql
│   └── optimize_vacuum.sql
│
└── docs/
    ├── architecture.md
    ├── exam_notes.md
    └── data_dictionary.md
```

---

## 📊 Data Model

### Core Tables

* **customers** – customer master data with KYC status
* **accounts** – bank accounts and balances
* **transactions** – debit/credit transactions
* **branches** – branch and regional mapping

These tables are processed across **Bronze, Silver, and Gold layers** using Delta Lake.

---

## 🔁 Key Engineering Practices Demonstrated

### Delta Lake

* Delta table creation
* INSERT / UPDATE / DELETE
* MERGE (CDC handling)
* Time Travel for audit & recovery
* Schema enforcement and evolution

### Spark

* DataFrame transformations
* Spark SQL for analytics
* Join strategies for fact/dimension data

### Governance & Performance

* Bronze/Silver/Gold separation
* Audit-friendly raw data preservation
* OPTIMIZE and ZORDER for performance

---


