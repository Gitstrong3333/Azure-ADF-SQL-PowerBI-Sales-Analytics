# Azure-ADF-SQL-PowerBI-Sales-Analytics
End-to-end Azure Data Engineering project using Azure Data Factory, Azure SQL Database, dimensional modeling, Power BI semantic model, and interactive sales reporting.
# Azure Data Factory to Power BI — End-to-End Sales Analytics

## Project Overview

Designed and implemented a cloud-based sales data pipeline using Azure Data Factory, Azure Blob Storage, Azure SQL Database, and Power BI.

The project demonstrates data ingestion, SQL staging, dimensional data warehouse design, pipeline orchestration, semantic modeling, DAX measures, and interactive business intelligence reporting.

## Technology Stack

- **Cloud Platform:** Microsoft Azure
- **Data Ingestion:** Azure Blob Storage, Azure Data Factory
- **Database:** Azure SQL Database
- **Programming:** T-SQL, SQL Stored Procedures
- **Data Modeling:** Star Schema, Fact and Dimension Tables
- **Business Intelligence:** Power BI Desktop
- **Analytics:** DAX Measures and Interactive Visualizations

## Solution Architecture

CSV Sales Data → Azure Blob Storage → Azure Data Factory → Azure SQL Staging → SQL Stored Procedures → Dimensional Data Warehouse → Power BI Semantic Model → Sales Performance Report

## Implementation

### 1. Data Ingestion

- Uploaded sales CSV data to Azure Blob Storage.
- Configured Azure Data Factory linked services and datasets.
- Created a Copy Data activity to load CSV records into an Azure SQL staging table.
- Parameterized the source filename for pipeline reusability.

### 2. Data Warehouse

Created the following tables:

- `DimCustomer`
- `DimProduct`
- `DimStore`
- `DimDate`
- `FactSales`

Implemented a star-schema design using surrogate keys and relationships between fact and dimension tables.

### 3. Pipeline Orchestration

- Configured stored procedure activities for dimensional and fact loading.
- Established activity dependencies.
- Executed and validated the pipeline successfully.
- Configured a daily schedule trigger, subsequently left stopped to avoid unnecessary executions.

### 4. SQL Validation

Validated the loaded fact data using SQL queries.

| Metric | Validated Result |
|---|---:|
| Sales Records | 10 |
| Unique Sales | 10 |
| Total Quantity | 18 |
| Total Sales | $3,780 |

### 5. Power BI Semantic Model

Imported the fact and dimension tables into Power BI Desktop.

Configured active many-to-one relationships and single-direction filtering from dimensions to the fact table.

Created DAX measures for:

- Total Sales
- Total Quantity
- Total Transactions
- Average Sale

### 6. Interactive Power BI Report

Developed a Sales Performance report featuring:

- Total Sales KPI
- Total Quantity KPI
- Total Transactions KPI
- Sales by Product
- Sales by City
- Daily Sales Trend
- Interactive Date Slicer

Validated slicer functionality by filtering the report to October 1, 2026, producing $1,350 in sales, 3 units, and 2 transactions.

 Key Skills Demonstrated

Azure Data Factory | Azure SQL | ETL/ELT | T-SQL | Stored Procedures | Dimensional Modeling | Star Schema | Data Validation | Power BI | DAX | Semantic Modeling

 Project Scope

The completed implementation demonstrates a working CSV-to-Power-BI reporting pipeline. Production-grade features such as comprehensive error handling, automated file archiving, and fully validated incremental loading remain potential future enhancements.

 Future Enhancements

- Implement robust incremental loads and upsert logic.
- Add automated data quality checks and failure notifications.
- Archive successfully processed files.
- Expand SCD Type 2 automation.
- Introduce monitoring and deployment automation.
