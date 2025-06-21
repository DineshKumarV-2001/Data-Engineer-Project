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

## Technologies Used
- Google Cloud Dataproc ( Spark , HDFS )
- PySpark
- Spark SQL
- Spark ML (for imputation)
- Google Cloud Bucket

## How to Run
1. Set up Dataproc cluster with provided configuration
2. Download dataset using the curl command
3. Run the notebook cells sequentially

## Key Insights
- Identified top-selling products and high-value customers
- Analyzed Top Sellers and Total Revenue Generated
- Calculated Total Revenue and Average Order Value (AOV) per Customers
- Discovered payment method preferences

## Downstreamed for Visualization & Further Analytics
- Merged All the Table's & Computed Columns to a Single Table
- Removed Unwanted/Invalid Columns 
- Fill Null Values Based on Column Criteria (eg:- mean for Payment , esitmated_delivery_date for missed delivery_date)
- Copied the Data to Google Bucket as in Parquet( best for Compression ) & can be Downloaded Directly from Google Bucket.
