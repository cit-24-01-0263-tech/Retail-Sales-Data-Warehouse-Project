# Retail Sales Data Warehouse Project

## Project Overview
This project demonstrates the design and implementation of a Retail Sales Data Warehouse using Python, Pandas and SQLite.

The project implements an ETL pipeline to extract, transform and load retail sales data into a dimensional data warehouse for analytical reporting.

## Data Warehouse Design
The warehouse follows a Star Schema consisting of:

- Dim_Customer
- Dim_Product
- Dim_Store
- Dim_Date
- Fact_Sales

Surrogate keys are used to connect the dimension tables with the fact table.

## ETL Pipeline
The ETL process includes:

1. Extracting retail sales source data
2. Data quality checking and staging
3. Transforming sales data
4. Calculating Gross Sales and Net Sales
5. Creating dimension and fact tables
6. Loading data into SQLite
7. Performing a second pipeline execution

## Slowly Changing Dimension (SCD Type 2)
SCD Type 2 is implemented for the Customer Dimension.

When a customer's city changes, the previous record is retained as historical data and a new record is created with a new surrogate key.

Example:

Kamal's city changed from Colombo to Kandy.

The old record is marked as historical and the new Kandy record is marked as the current record.

## Second Pipeline Execution
The second pipeline execution demonstrates:

- Changed customer handling
- New customer insertion
- Unchanged customer handling
- Surrogate key management
- New fact record loading

## Analytical Queries
The project includes analysis of:

- Sales performance by product
- Sales performance by store
- Customer sales performance
- Total net sales
- Transaction counts

## Validation Results
Final validation confirmed:

- 13 Fact Records
- 7 Customer Dimension Records
- 6 Current Customers
- 1 Historical Customer Record
- Total Net Sales: 1,193,500
- 0 Duplicate Transaction IDs
- 0 Missing Customer Keys

## Technologies Used
- Python
- Pandas
- SQLite
- Google Colab
- GitHub

## Project File
`Retail_Sales_Data_Warehouse_Project.ipynb`
