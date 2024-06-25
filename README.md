# Building a Real-Time Data Pipeline with AWS, DynamoDB, and Snowflake
-------------------------------------------------------------
![dynamo drawio](https://github.com/bhavanachitragar/Building-a-Real-Time-Data-Pipeline-with-AWS-DynamoDB-and-Snowflake-/assets/91766461/10b593aa-6c94-4988-a6a0-41a63df191b3)


This project builds a real-time data pipeline using AWS services and Snowflake. It starts with an AWS Lambda function that periodically fetches weather data from an API and stores it in a DynamoDB table. DynamoDB Streams capture changes and trigger another Lambda function to write the data to an S3 bucket in CSV format. Snowpipe in Snowflake automatically ingests the data from S3, making it available for analysis and visualization within Snowflake. This setup ensures continuous, automated data flow and real-time insights from the weather data.

#### AWS services used:

- AWS Lambda
- AWS DynamoDB
- S3 
- IAM


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
#### DynamoDB
![Screenshot 2024-06-25 132004](https://github.com/bhavanachitragar/Building-a-Real-Time-Data-Pipeline-with-AWS-DynamoDB-and-Snowflake-/assets/91766461/7cc97b83-62de-4f66-9070-ee4967487ee1)
### S3 Bucket
![Screenshot 2024-06-25 134246](https://github.com/bhavanachitragar/Building-a-Real-Time-Data-Pipeline-with-AWS-DynamoDB-and-Snowflake-/assets/91766461/e11579e6-2f57-4517-8198-170a2d8829f1)
### Snowflake
![Screenshot 2024-06-25 141025](https://github.com/bhavanachitragar/Building-a-Real-Time-Data-Pipeline-with-AWS-DynamoDB-and-Snowflake-/assets/91766461/bf7e944f-bc57-4d1b-bc74-968f5d803e9f)



### Output:

![Screenshot 2024-06-25 143133](https://github.com/bhavanachitragar/Building-a-Real-Time-Data-Pipeline-with-AWS-DynamoDB-and-Snowflake-/assets/91766461/0ed2df90-cd30-4c1a-a68d-4f16aec71dbd)

----------------------------------------------------------------

#### Credits: DateWithData
