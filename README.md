# Telco Customer Data Engineering Project

## Project Overview

This project involves automating the data pipeline for the Telco customer churn dataset. The goal is to create an efficient ETL (Extract, Transform, Load) process that ingests data from an Amazon S3 bucket, catalogs it using AWS Glue, and loads it into Amazon Redshift for analysis and visualization. The entire process will be orchestrated using Apache Airflow, and data visualization will be done using Power BI. Additionally, Amazon Athena will be used to query the Glue Data Catalog.

## Project Architecture

![Customer Churn ETL pipeline](https://github.com/tejasjbansal/Customer-Churn-Data-Analytics/assets/56173595/2c4b6ef9-f567-46c6-918a-0fcbad007dd8)

## Dataset

**Telco Customer Churn Dataset**: This dataset is used to analyze customer churn in a telecommunications company. It includes various customer details, services used, account information, and whether the customer has churned.

- **Source**: [Kaggle - Telco Customer Churn Dataset](https://www.kaggle.com/datasets/yeanzc/telco-customer-churn-ibm-dataset?resource=download)

## Project Requirements

### Tools and Technologies

1. **Amazon S3**: Storage for the raw data files.
2. **AWS Glue**: Data cataloging and ETL jobs.
3. **Amazon Redshift**: Data warehouse for storing processed data.
4. **Apache Airflow**: Workflow orchestration.
5. **Power BI**: Data visualization.
6. **Amazon Athena**: SQL queries on the Glue Data Catalog.

### Steps to Complete the Project

1. **Set Up Amazon S3 Bucket**:
   - Create an Amazon S3 bucket to store the raw data files from the upstream process.

2. **Create AWS Glue Crawler**:
   - Set up an AWS Glue Crawler to crawl the S3 bucket and create a Glue Data Catalog.

3. **Create AWS Glue Job**:
   - Develop an AWS Glue job to process the data and load it into Amazon Redshift.

4. **Set Up Amazon Redshift**:
   - Create an Amazon Redshift cluster and set up the necessary tables for the processed data.

5. **Orchestrate with Apache Airflow**:
   - Configure Apache Airflow to trigger the Glue job and manage the workflow.

6. **Visualize with Power BI**:
   - Connect Power BI to Amazon Redshift for data visualization and analysis.

7. **Query with Amazon Athena**:
   - Use Amazon Athena to run SQL queries on the Glue Data Catalog.

## Getting Started

### Prerequisites

- Ensure you have all required AWS services set up.
- Install necessary Python packages:
  ```bash
  bash setup.sh
  ```
  
## Detailed Steps

### Step 1: Set Up Amazon S3 Bucket

- **Create an S3 Bucket**: Log into the AWS Management Console, navigate to the S3 service, and create a new bucket.
- **Upload Dataset**: Download the Telco Customer Churn dataset from Kaggle and upload the files to the S3 bucket.

### Step 2: Create AWS Glue Crawler

- **Create Crawler**: In the AWS Glue console, create a new crawler.
- **Configure Crawler**: Point the crawler to the S3 bucket and configure it to crawl the data.
- **Run Crawler**: Execute the crawler to create the Glue Data Catalog.

### Step 3: Create AWS Glue Job

- **Develop Glue Job**: In the AWS Glue console, create a new Glue job.
- **Job Script**: Write a script to extract data from the S3 bucket, transform it, and load it into Amazon Redshift.
- **Run Job**: Test and run the Glue job.

### Step 4: Set Up Amazon Redshift

- **Create Redshift Cluster**: Set up a new Amazon Redshift cluster.
- **Create Tables**: Define the schema and create tables in Redshift for storing the processed data.

### Step 5: Orchestrate with Apache Airflow

- **Install Apache Airflow**: Set up Apache Airflow on an Amazon EC2 instance or use AWS Managed Workflows for Apache Airflow.
- **Define DAG**: Create a Directed Acyclic Graph (DAG) in Airflow to automate the workflow.
- **Configure Tasks**: Set up tasks in Airflow to trigger the Glue job and manage the process.

### Step 6: Visualize with Power BI

- **Connect to Redshift**: In Power BI, connect to the Amazon Redshift cluster.
- **Create Reports**: Develop reports and dashboards to visualize the data.

### Step 7: Query with Amazon Athena

- **Configure Athena**: Set up Amazon Athena to query the Glue Data Catalog.
- **Run Queries**: Use Athena to write and execute SQL queries to analyze the data.

## Conclusion

By following these steps, you will have an automated data pipeline that ingests, processes, and visualizes data from the Telco Customer Churn dataset. This project demonstrates how to integrate various AWS services and tools to build a robust data engineering solution.

For any questions or assistance, please refer to the documentation of the respective AWS services or reach out to the project supervisor.
