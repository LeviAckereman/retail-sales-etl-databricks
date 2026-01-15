# Retail Sales ETL Pipeline 

This project demonstrates a simple end-to-end ETL pipeline built on Databricks using PySpark and Delta Lake.  
The goal was to understand how raw data is ingested, cleaned, and transformed into business-ready tables.

---

## What this project does

The pipeline processes retail sales data using the Bronze–Silver–Gold approach:

- **Bronze layer**: Raw CSV data is loaded and stored as a Delta table without any changes.
- **Silver layer**: Data is cleaned by removing cancelled orders and records with missing customer information.
- **Gold layer**: Monthly revenue is calculated from the cleaned data.

---

## Tools used

- Databricks (Serverless)
- PySpark
- Spark SQL
- Delta Lake

---

## Dataset

The project uses an online retail dataset containing transaction-level sales data such as:
Invoice number, product code, quantity, invoice date, unit price, and customer ID.

---

## Key points

- Raw CSV data is converted into Delta tables for reliable processing.
- Date fields stored as strings are explicitly converted to timestamps.
- The pipeline is structured so that raw data can always be reprocessed if business rules change.

---

## How to run

1. Upload the dataset to a Databricks Volume.
2. Run the notebook cells in order:
   - Bronze ingestion
   - Silver cleaning
   - Gold aggregation
3. Delta tables are written inside Databricks Volumes.

---

## Notes

This project focuses on core data engineering concepts such as ETL flow, data cleaning, and Delta Lake usage.  
It does not include dashboards or scheduling.

---

## Author

Aditya Pagar
