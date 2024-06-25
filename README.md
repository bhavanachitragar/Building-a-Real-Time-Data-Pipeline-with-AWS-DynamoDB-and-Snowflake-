# Building a Real-Time Data Pipeline with AWS, DynamoDB, and Snowflake
-------------------------------------------------------------

This project builds a real-time data pipeline using AWS services and Snowflake. It starts with an AWS Lambda function that periodically fetches weather data from an API and stores it in a DynamoDB table. DynamoDB Streams capture changes and trigger another Lambda function to write the data to an S3 bucket in CSV format. Snowpipe in Snowflake automatically ingests the data from S3, making it available for analysis and visualization within Snowflake. This setup ensures continuous, automated data flow and real-time insights from the weather data.

#### AWS services used:

1- AWS Lambda
2- AWS DynamoDB
3- S3 
4- IAM


### 1. AWS Lambda
In this project, one Lambda function fetches weather data from an external API and stores it in DynamoDB, while another processes DynamoDB Streams and writes data to an S3 bucket in CSV format.

### 2. Amazon DynamoDB
Amazon DynamoDB stores real-time weather data fetched by AWS Lambda. It uses DynamoDB Streams to capture changes in the data, triggering another Lambda function for further processing.

### 3. Amazon S3
Amazon S3 is used to store raw data files (in CSV format) from DynamoDB. These files are then ingested by Snowflake using Snowpipe for analysis.

### 4. AWS IAM
AWS IAM manages permissions and roles for AWS services. It ensures that Lambda functions have the necessary access to interact with DynamoDB and S3, maintaining secure and controlled access.

### 5. Snowflake
Snowflake is used to automatically ingest data from S3 via Snowpipe, making the data available for real-time analysis and reporting.

#### Sanpshots:
 

### Output
----------------------------------------------------------------

#### Credits: DateWithData
