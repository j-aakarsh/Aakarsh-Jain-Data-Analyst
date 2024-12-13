# Aakarsh Jain's Data Analysis Projects
# University Grade Appeals Analysis

## Project Description
Analyzing university grade appeal data to identify patterns in the appeal process and outcomes, improving the process by understanding time spent on form filling and the reasons for appeal refusals.

## Project Title
University Grade Appeals Analysis: An Exploratory, Descriptive, and Diagnostic Data Study

## Objective
The primary goal of this project is to perform an exploratory, descriptive, and diagnostic analysis on the university's grade appeal dataset to uncover patterns, trends, and insights related to appeal decisions. By analyzing various features and integrating clickstream data, we aim to understand factors influencing appeal outcomes and improve the form-filling process.

## Motivation
The aim of this project was to identify why some grade appeals were denied due to improper or incomplete form filling. By analyzing the clickstream data, which tracked the time students spent on each form page, it was hypothesized that the complexity or confusion in the form-filling process could be a contributing factor. This insight could then be used to improve the appeal process by simplifying the forms or providing better guidance to students.

## Dataset
### Grade Appeals Dataset
- **Appeal_ID**: Unique identifier for each appeal.
- **Student_ID**: Identifier for the student.
- **Appeal_Type**: Type of appeal (e.g., grade correction, re-evaluation).
- **Appeal_Status**: Current status of the appeal (e.g., submitted, under review, resolved).
- **Decision**: Outcome of the appeal (e.g., approved, denied).
- **Submission_Date**: Date the appeal was submitted.
- **Review_Committee**: Committee responsible for reviewing the appeal.
- **Resolution_Date**: Date the appeal was resolved.
- **Term_Appealed**: Term during which the appeal was filed.
- **Notes**: Additional comments or notes related to the appeal.

### Clickstream Dataset
- **Appeal_ID**: Unique identifier linking clickstream data to the appeal.
- **Student_ID**: Identifier for the student.
- **Action**: Specific action taken by the student (e.g., page visit, form submission).
- **Action_Timestamp**: Timestamp of when the action occurred.
- **Page_URL**: URL of the page where the action took place.
- **Session_ID**: Unique identifier for the user's session.
- **Duration**: Time spent on the action/page.
- **Page_Visited**: Indicator of the page that was visited.

## Methodology
### Descriptive Analysis
1. **Data Collection and Preparation**:
   - Ingest the grade appeals data and clickstream data into Amazon S3.
   - Profile and clean the data using AWS Glue DataBrew, handling missing values, and formatting columns.
   - ![Data Ingestion](path/to/your/data_ingestion_screenshot.png) _**(Insert a screenshot of your data in the S3 bucket)**_

2. **Descriptive Statistics**:
   - Generate summary statistics for numerical features and frequency distributions for categorical features.
   - ![Summary Statistics](path/to/your/summary_statistics_screenshot.png) _**(Insert a screenshot of the summary statistics)**_

### Diagnostic Analysis
3. **Data Profiling & Cleaning**:
   - Remove unwanted columns, replace missing values, and format date columns.
   - Create an ETL pipeline using AWS Glue to join the datasets.
   - ![Data Cleaning](path/to/your/data_cleaning_screenshot.png) _**(Insert a screenshot of the DataBrew interface)**_

4. **Security Enhancements**:
   - Enable encryption using AWS KMS-generated keys.
   - Implement S3 bucket versioning and backup through replication rules.
   - Apply lifecycle rules to optimize storage costs.

### Exploratory Analysis
5. **Data Analysis and Visualization**:
   - Use AWS Glue crawlers to create a relational database and generate tables.
   - Run SQL queries in AWS Athena to analyze the average time spent on form filling and identify patterns in appeal outcomes.
   - ![SQL Queries](path/to/your/sql_queries_screenshot.png) _**(Insert a screenshot of the Athena SQL query results)**_
   - Create visualizations using AWS ETL Dashboard to illustrate key insights.
   - ![Visualization](path/to/your/visualization_screenshot.png) _**(Insert a screenshot of your visualizations)**_

### Descriptive and Diagnostic
6. **Monitoring and Alerts**:
   - Create a dashboard in AWS CloudWatch to monitor service usage and costs.
   - Set up alarms to notify if cost thresholds are reached.
   - ![CloudWatch Dashboard](path/to/your/cloudwatch_dashboard_screenshot.png) _**(Insert a screenshot of the CloudWatch dashboard)**_

## Insights and Findings
- Analysis of time spent on form filling revealed that complicated forms led to higher appeal denial rates due to incomplete or incorrect submissions.
- Implemented measures to improve form clarity and guidance for students.

## Conclusion
By analyzing the university's grade appeal data and integrating clickstream data, we were able to uncover key factors contributing to appeal outcomes. These insights will help in streamlining the appeal process and enhancing form usability.

## Tools and Technologies
- **Storage**: Amazon S3
- **Data Profiling & Cleaning**: AWS Glue DataBrew
- **Server**: Amazon EC2 (VPC Server)
- **Data Collection**: Clickstream data collection platform
- **Data Quality & ETL**: AWS Glue
- **Data Analysis**: AWS Athena, SQL
- **Visualization**: AWS ETL Dashboard
- **Security**: AWS KMS, S3 Versioning, Replication Rule, Lifecycle Rule
- **Monitoring**: AWS CloudWatch

