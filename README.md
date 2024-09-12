# Incremental_Load_Pyspark

## Purpose
This project demonstrates how to efficiently perform incremental data loading using a Jupyter Notebook (`incremental_load.ipynb`). Incremental data loading refers to updating only the new or changed records from a data source rather than reloading the entire dataset. This is particularly useful for large datasets where full reloads are computationally expensive or time-consuming.

## Features
- **Incremental Load Logic:** Implements logic to identify and load only new or updated records.
- **Data Source Integration:** Can integrate with databases, files, or API endpoints.
- **Efficiency:** Reduces load times by avoiding unnecessary data duplication.
- **Customizable:** Easily adaptable to different data formats and schemas.

## Prerequisites 
- Databricks Community Edition
- Python
- Pyspark
- SQL

## How To Use The Code
- Perform the Initial load (Full Load), By loading the table into the DBFS in delta format (load).
- Note the maximum modified date into another delta table (watermark_table)
- When the new data arrives compare the date from watermark_table and store the new data into the old table (load).
- Update the watermark_table with the new maximum modified table.
