# **Data Extraction From Olist**
 
A new directory named `olist` was created to organize the project files for the data engineering workflow. The [Olist Brazilian E-commerce dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)  was downloaded directly from Kaggle using a `curl` command within a Bash script, executed through a remote SSH terminal.
 

#!/bin/bash curl -L -o ~/olist/[brazilian-ecommerce.zip](http://brazilian-ecommerce.zip)  [https://www.kaggle.com/api/v1/datasets/download/olistbr/brazilian-ecommerce](https://www.kaggle.com/api/v1/datasets/download/olistbr/brazilian-ecommerce) 
 

**After downloading the dataset:**
 
 *The ZIP file was extracted using :-* 
 
***standard unzip command :*  unzip** [**brazilian-ecommerce.zip**](http://brazilian-ecommerce.zip)  **-d ~/olist/dataset/**
 

*   A new subdirectory named `dataset` was created inside the main `olist` directory.
     
*   All the extracted `.csv` files were moved into the `dataset` folder for structured data storage and easier access during the ETL process.
     

# **Data Injection to Hadoop Cluster**
 
The olist datasets was injected into the Hadoop Distributed File System (HDFS) to enable distributed storage and parallel processing using the Hadoop ecosystem.
 

## **📁 HDFS Directory Creation:**
 
A new directory was created in HDFS to store the CSV files related to the Olist project: **hadoop fs -mkdir -p  */data/olist/***
 

## **📤Uploading CSV Files to HDFS:**
 
All CSV files from the local project directory (~/olist/dataset) were copied to the HDFS directory ***/data/olist*** using the hadoop fs -put
 
command: **hadoop fs -put ~/olist/dataset/\*.csv /data/olist/**