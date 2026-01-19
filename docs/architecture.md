# ApexTrust Bank – Lakehouse Documentation

Technology used: *sql, python, ipython-sql*

## Abstract

architecture.md
1. High-Level Architecture
The ApexTrust Bank project follows the Databricks Lakehouse architecture using the Medallion pattern (Bronze–Silver–Gold). This design combines the reliability of data warehouses with the flexibility of data lakes.
Core Components:
-   Databricks Workspace
-   Apache Spark
-   Delta Lake
-   Unity Catalog
-   Cloud Object Storage


2. Medallion Architecture
-  Bronze Layer (Raw Data)
-   Stores raw ingested data from CSV files
-   No business rules applied
-   Schema enforced but data preserved as-is
-   Acts as an immutable audit layer


    Tables:
    - customers
    - accounts
    - transactions
    - branches
    - cdc_customers

    Silver Layer (Validated Data)
    -  Applies business rules and data cleansing
    -   Deduplication and type casting
    -   Enforces domain constraints (e.g., VERIFIED customers, non-negative balances)
    
    Gold Layer (Analytics)
    -  Aggregated, business-ready data
    -   Used for reporting and BI
    -   Optimized for query performance
----

Delta Lake Capabilities Used
-      ACID Transactions
-       MERGE (CDC handling)
-       Time Travel (audit & rollback)
-       OPTIMIZE & VACUUM
-       Schema Enforcement & Evolution
