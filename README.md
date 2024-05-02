# -ETL-with-Python
End-to-End ETL Pipeline Using Python
Information Technology Institute (ITI) - Data Management Track (Intake 44/2024)
Overview
This project aims to design and implement an end-to-end Extract, Transform, Load (ETL) process for a bicycle store using Python. It covers the entire data processing workflow from database setup to data modeling and visualization. The ETL pipeline handles data from various sources, including databases, data lakes, and APIs, and incorporates rigorous data quality checks, transformations, and loading into a structured data model for analytics.

Project Structure
The project is organized into five main stages, each contributing to the overall ETL pipeline. Here's an overview of the stages:

Stage 1: Database and Data Lake Setup
Database Creation: Setting up a PostgreSQL database with schemas and tables for storing order and item data.
Data Lake Configuration: Creating folders within a cloud storage solution to hold additional data, like CSV files from different departments.
Stage 2: Data Extraction
Database Extraction: Extracting data from PostgreSQL using custom SQL queries.
Data Lake Extraction: Reading files from the data lake folder structure.
API Integration: Fetching real-time exchange rates and storing them in the landing folder.
Data Consolidation: Combining all extracted data into a single CSV file per dataset, enriched with metadata like extraction timestamp and data source.
Stage 3: Data Quality Checks
Null Checks: Identifying and handling null values in essential fields.
Duplicate Checks: Detecting and removing duplicate rows.
Data Validation: Ensuring data types and values are within expected ranges (e.g., price ranges, date limits).
Preparation for Staging: Storing cleaned and validated data in 'staging_1' folder for transformation.
Stage 4: Data Transformation
Currency Conversion: Merging latest currency exchange rates to calculate local prices.
Delivery Metrics: Adding columns to track delivery performance, such as late deliveries and latency days.
Locality Flag: Determining if customers are local based on proximity to stores.
Lookup Tables: Resolving ambiguous columns by creating and utilizing lookup tables for order statuses.
Transformed Data Staging: Outputting transformed data to 'staging_2' for further processing.
Stage 5: Data Modeling and Visualization
Data Merging: Integrating orders, items, and product details into a unified dataset for deeper analysis.
Visualization Creation: Developing at least three types of visualizations to illustrate key metrics and trends.
Documentation: Documenting the modeling techniques and visualization choices.
Result Compilation: Organizing final datasets and visualizations in 'Information Mart' and 'Visualization' folders respectively.
Final Deliverables
Python Scripts and Jupyter Notebooks: Documented code for each stage of the ETL process.
Clean and Transformed Datasets: Data ready for analysis in structured folders.
Visualizations and Analytical Reports: Demonstrating the insights derived from the data.
