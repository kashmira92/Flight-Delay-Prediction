# DataEngineering_on_YouTube_Videos

A comprehensive ETL (Extract, Transform, Load) pipeline designed to ingest, transform, and organize YouTube video stats from various sources into a format suitable for streamlined analysis. Here's a breakdown of the key components and steps involved in your project:

1. **Infrastructure Setup:**
   - Utilized AWS services like S3, Glue, Lambda, IAM, AWS CLI, Athena, and CloudWatch.
   - Implemented IAM groups and roles with the least privilege policy to ensure security.
   - Leveraged AWS CLI for data ingestion into AWS services.

2. **ETL Pipeline Design:**
   - Used Glue for discovering and extracting metadata from different data sources.
   - Employed Glue Crawlers to create the Glue Catalog, which stores information about the data.
   - Transformed data into Parquet format for optimized storage and efficient analysis.
   - Utilized AWS Lambda for preprocessing and transformation tasks, converting JSON to Parquet format.
   - Managed IAM roles for Lambda functions to access necessary AWS resources securely.
   - Utilized AWS Wrangler to access and read files stored in S3 buckets.
   - Implemented AWS Lambda Layers for packaging necessary libraries conveniently.

3. **Data Transformation:**
   - Ensured JSON data conforms to Glue requirements (single line format) for proper processing.
   - Converted JSON data to Parquet format for efficient storage and querying.

4. **Data Analysis and Querying:**
   - Leveraged AWS Athena for ad-hoc querying of data stored in Glue Catalog.
   - Optimized data organization through partitioning based on regions and category IDs.

5. **Automation and Monitoring:**
   - Implemented automation using Glue Jobs for scheduled ETL tasks.
   - Enabled CloudWatch logging for monitoring job metrics and performance.

6. **Reporting and Visualization:**
   - Utilized Glue Studio for data visualization and manipulation.
   - Combined and joined datasets from cleaned CSV and JSON tables for reporting purposes.
   - Stored the resulting data in a target S3 bucket partitioned for regions and category IDs.

The project demonstrates a robust ETL pipeline leveraging various AWS services for data processing, transformation, and analysis, with a focus on security, efficiency, and automation. 
