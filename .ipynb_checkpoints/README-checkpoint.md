# Project: Data Warehouse
## Project Overview
A music streaming startup, Sparkify, has grown their user base and song database and want to move their processes and data onto the cloud. Their data resides in S3, in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.

In this project, we will create an ETL pipeline to build a data warehouses hosted on Redshift. We will need to load data from S3 to staging tables on Redshift and execute SQL statements that create the analytics tables from these staging tables.
## Song Dataset
We will be working with 2 datasets that reside in S3.
## Log Dataset
The second dataset consists of log files in JSON format generated by this event simulator based on the songs in the dataset above.
## Files in Project
1. README.md - Overview of project. Includes information about the components of the project and how to run it
2. create_cluster_redshift.ipynb - Run notebook to create and delete redshift cluster, as well as running the ETL process defined in other scripts
3. etl.py - Contains script to run ETL process
4. sql_queries.py - Contains script for the framework of the necessary tables
5. create_tables.py - Contains script to create the necessary tables
6. dwh.cfg - Contains information around AWS Access and security

## Schema for Song Play Analysis
### Fact Table
songplays
### Dimension Tables
users
songs
artists
time
## ETL objective
Extracting data from S3 and loading them into Redshift for analytics purpose.
## Data Transfer and Reasoning
The logs for Sparkify are stored in a JSON format in S3. To use any of the data for analytics purpose, we need to load the data in a consumable manner into Redshift. Once the transformed data is loaded into Redshift, the analytics team can gain insight on the data found in the logs.

