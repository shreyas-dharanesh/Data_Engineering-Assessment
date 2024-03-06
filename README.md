# Data_Engineering-Assessment
PEI Group

## Prerequisite:
### Databricks
* Databricks Community Edition

### Install Spark excel reading packge:
1. To read data from excel into a Pyspark dataframe
2. Go to the Cluster configurations
3. Select libraries and select Maven
4. Enter "com.crealytics:spark-excel_2.12:0.13.5" in the Coordinate field and click Install

## Project Flow:
1. Import packages
2. Read Order data from json 
    * Format price column: Extract price information and ignore invalid characters
    * DataType Casting and schema validation
3. Read Customer data from xlsx
    * Format customer name: Remove invalid characters and extra whitespaces
    * Format phone number: Extract numbers only, remove leading country code 001
    * DataType Casting and schema validation
5. Read Product data from csv
    * Verify state: Check if US state information is correct
    * DataType Casting and schema validation
7. Save order, customer, product dataframes into delta table
8. Create enriched tables for each use case as per the requirment
9. Run SQL queries on the saved delta tables with Spark SQL commands

## Overview on the workflow:
