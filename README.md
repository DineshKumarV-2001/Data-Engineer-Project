# Olist-Data-Engineer-Project
# Brazilian E-Commerce Data Analysis with PySpark

## Project Overview
- Analyzed Olist's Brazilian e-commerce dataset using PySpark on Google Cloud Dataproc
- Processed 9 datasets with ~100K-1M records each
- Implemented data cleaning, transformation, Imputation and advanced analytics

## Key Features
- Data extraction from Kaggle to HDFS 
- Comprehensive data validation and cleaning
- Customer segmentation and seller performance analysis
- Optimized Spark joins and performance tuning
- Used Cache for Iterative Datasets
- Used SparkML Feature : Imputer - to fill missing (null/NaN) values in numeric columns with a statistical strategy(Mean, Median, Mode).
![Screenshot 2025-06-21 204136](https://github.com/user-attachments/assets/488cb756-5089-4c44-8afc-919104bb296d)

 

## Technologies Used
- Google Cloud Dataproc ( Spark , HDFS )
- PySpark
- Spark SQL
- Spark ML (for imputation)
- Google Cloud Bucket

## Key Insights
- Identified top-customers by spending.
- ![Screenshot 2025-06-21 203008](https://github.com/user-attachments/assets/64bd4556-7be3-444c-96c5-a33182f813ce)

- Analyzed Sellers Performance Metrics
- ![image](https://github.com/user-attachments/assets/328bf3ef-d748-4fff-b2e5-0939beb923ff)

- Calculated Total Revenue and Average Order Value (AOV) per Customers
- ![Screenshot 2025-06-21 202844](https://github.com/user-attachments/assets/b8a4e5c0-439d-4936-969f-a6a6cab3aa61)

- Customer Segmentation by Total Spending
- ![image](https://github.com/user-attachments/assets/d67e3547-633f-4fd3-b39a-61ceb9fa59bf)


## Downstreamed for Visualization & Further Analytics
- Merged All the Table's & Computed Columns to a Single Table
- Removed Unwanted/Invalid Columns 
- Fill Null Values Based on Column Criteria (eg:- mean for Payment , esitmated_delivery_date for missed delivery_date)
- Copied the Data to Google Bucket as in Parquet( best for Compression ) & can be Downloaded Directly from Google Bucket.
