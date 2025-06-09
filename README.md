# Orbital-Insights-
Transforming UCS Satellite Database into actionable insights with Snowflake stored procedures and Python pipelines
End-to-End Data Pipeline & Analytics Platform for Satellite Data Using Snowflake and Python



📑 Table of Contents
Project Overview
Dataset Description
Architecture
Technologies Used
Data Ingestion & Storage
Data Transformation & Cleaning
Snowflake Setup
Stored Procedures
Python Integration
Data Quality & Validation
CI/CD Pipeline (Optional)
Insights & Analysis
Project Setup Instructions
Future Enhancements
Acknowledgements


#1. Project Overview
This project aims to build a scalable, end-to-end data pipeline and analytics solution using the UCS Satellite Database. It demonstrates skills in data engineering, Snowflake SQL, stored procedures, Python ETL, data quality validation, and (optionally) CI/CD automation.

#2. Dataset Description
Source: UCS Satellite Database (Excel file)
Description: Contains satellite metadata including name, country, operator, launch date, orbit class, purpose

#3. Architecture
Data Source → Python ETL → AWS S3 → Snowflake → Stored Procedures → Analytics
(Optional) GitHub Actions CI/CD for automation

#4. Technologies Used
Snowflake: Cloud data warehouse, stored procedures, Snowpark (optional)
Python: ETL, data cleaning, API integration
AWS S3: Cloud storage for data files
pandas/openpyxl: Excel parsing
snowflake-connector-python: Connecting to Snowflake
Great Expectations: (optional) Data validation

#5. Data Ingestion & Storage
Parse UCS Satellite Database Excel file using Python
Store cleaned CSV locally or in AWS S3 bucket
Snowflake: Create staging tables and define file formats

#6. Data Transformation & Cleaning
Standardize country/operator names
Parse dates and handle missing values
Validate numerical fields (mass, lifetime)
Prepare data for Snowflake ingestion

#7. Snowflake Setup
Create database and schema
Define table schemas
Load data into Snowflake tables
Configure file formats and stages

#8. Stored Procedures
satellites_by_country(): Aggregates satellite counts by country
orbit_distribution(): Aggregates satellites by orbit type
launch_trends(): Year-over-year analysis of satellite launches

#9. Python Integration
Use snowflake-connector-python to:
Load data into Snowflake
Call stored procedures
Fetch query results

#10. Data Quality & Validation
Null checks
Data type validations
Range validations for numerical fields
(Optional) Implement Great Expectations suite

#11. CI/CD Pipeline (Optional)
Use GitHub Actions to:
Run Python ETL tests on pull requests
Automate scheduled data pipeline runs
Validate data quality before deployment

#12. Insights & Analysis
Satellites by country/operator
Orbit class usage distribution
Launch trends over time
(Optional) Additional business insights (e.g. operator market share)

#13. Project Setup Instructions
Clone this repository
Create a Snowflake trial account
Configure AWS S3 (optional)
Install Python dependencies
Update connection parameters in config.py
Run etl_pipeline.py to load data
Execute stored procedures from Snowsight or Python

#14. Future Enhancements
Integrate with real-time satellite tracking APIs
Add geospatial analysis with Snowflake’s geospatial functions
Visualize insights with Power BI or Tableau
Enhance CI/CD pipeline with data validation steps

#15. Acknowledgements
UCS Satellite Database (source data)
Snowflake community documentation
