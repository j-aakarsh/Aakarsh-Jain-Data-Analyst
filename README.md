# Aakarsh Jain
# 👋 About Me  
Hi! I'm a passionate **Data Analyst** and aspiring **Machine Learning Enthusiast** with a background in **Mechanical Engineering** and an MBA specializing in **AI applications**. I thrive at the intersection of technology and innovation, exploring data-driven solutions for real-world challenges.  

## 🔍 What I Do  
- 🧠 Built machine learning models, including a **KNN-based clustering model** for banking credit card data.  
- 🛠 Developed pipelines for **ETL processes** using **AWS Glue** for scalable data integration.  
- 📊 Designed interactive data visualizations for effective storytelling and decision-making.  
- 🌱 Advocating for sustainable and innovative research through data insights.  

## 👨‍💻 Let's Collaborate  
I'm always open to collaborating on projects related to **data engineering**, **machine learning**, and **renewable energy**. Let's create something impactful together!  

🌟 *"Exploring the infinite possibilities hidden in data!"*

## 📂 My Projects 

# 1. 📊 Analysis of University Canada West's Grade Appeal Process

---

## ✨ Project Description

Analyzing university grade appeal data to identify patterns in the appeal process and outcomes, improving the process by understanding time spent on form filling and reasons for appeal refusals.

---

## 🏷️ Project Title

**University Grade Appeals Analysis:** An Exploratory, Descriptive, and Diagnostic Data Study

---

## 🎯 Objective

To perform exploratory, descriptive, and diagnostic analyses on the university's grade appeal dataset, uncovering patterns, trends, and insights related to appeal decisions. By integrating clickstream data, we aim to enhance the form-filling process and improve appeal outcomes.

---

## 💡 Motivation

This project aims to identify why some grade appeals were denied due to improper or incomplete form filling. By analyzing clickstream data tracking time spent on each form page, we hypothesized that complexity or confusion in the form-filling process contributes to denials. Insights will help simplify forms and provide better guidance to students.

---

## 📂 Datasets

### **1. Grade Appeals Dataset**

| **Field**             | **Description**                                         |
|-----------------------|-------------------------------------------------------|
| **Appeal_ID**         | Unique identifier for each appeal                     |
| **Student_ID**        | Identifier for the student filing the appeal          |
| **Appeal_Type**       | Type of appeal (e.g., grade correction, re-evaluation) |
| **Appeal_Status**     | Current status of the appeal                          |
| **Decision**          | Outcome of the appeal                                 |
| **Submission_Date**   | Date the appeal was submitted                         |
| **Review_Committee**  | Committee reviewing the appeal                        |
| **Resolution_Date**   | Date the appeal was resolved                          |
| **Term_Appealed**     | Academic term when the appeal was filed               |
| **Notes**             | Additional comments or notes                         |

### **2. Clickstream Dataset**

| **Field**             | **Description**                                          |
|-----------------------|----------------------------------------------------------|
| **Appeal_ID**         | Links clickstream data to the corresponding appeal       |
| **Student_ID**        | Identifier for the student interacting with the form     |
| **Action**            | Specific action taken (e.g., page visit, submission)     |
| **Action_Timestamp**  | Timestamp of the action                                  |
| **Page_URL**          | URL of the page where the action occurred               |
| **Session_ID**        | Unique identifier for the session                       |
| **Duration**          | Time spent on the specific action or page               |
| **Page_Visited**      | Page being interacted with                              |

### 🛠️ **Why These Datasets?**

- **Grade Appeals Dataset**: Understand the nature, resolution, and outcomes of appeals.
- **Clickstream Dataset**: Gain insights into user behavior and identify form-filling challenges.

---

## 🔬 Methodology

### 1️⃣ Descriptive Analysis

1. **Data Collection & Preparation**:
   - Ingest grade appeals and clickstream data into **Amazon S3**.
   - Profile and clean data using **AWS Glue DataBrew**, handling missing values and formatting columns.

2. **Descriptive Statistics**:
   - Generate summary statistics for numerical features and frequency distributions for categorical features.

### 2️⃣ Diagnostic Analysis

3. **Data Profiling & Cleaning**:
   - Remove irrelevant columns, replace missing values, and format dates.
   - Create an ETL pipeline using **AWS Glue** to join datasets.

4. **Security Enhancements**:
   - Enable encryption using **AWS KMS**.
   - Implement **S3 bucket versioning** and backups with replication rules.
   - Apply lifecycle rules to optimize storage costs.

### 3️⃣ Exploratory Analysis

5. **Data Analysis & Visualization**:
   - Use **AWS Glue crawlers** to generate relational database tables.
   - Run SQL queries in **AWS Athena** to analyze form-filling time and appeal outcome patterns.
   - Visualize insights using **AWS ETL Dashboard**.

### 4️⃣ Monitoring & Alerts

6. **Monitoring Costs**:
   - Create a dashboard in **AWS CloudWatch** to monitor service usage and costs.
   - Set up alarms for cost threshold breaches.

---

## 📈 Insights & Findings

- 🕒 **Form-Filling Duration**: Complicated forms correlated with higher denial rates due to incomplete submissions.
- 📝 **Improved Clarity**: Suggested measures to enhance form clarity and student guidance.

---

## 🏁 Conclusion

By integrating clickstream data and analyzing university grade appeals, we uncovered factors affecting appeal outcomes and identified ways to streamline the process. These findings aim to enhance user experience and improve the success rate of appeals.

---

## 🛠️ Tools & Technologies

| **Category**         | **Tool**                       |
|----------------------|-------------------------------|
| **Storage**          | Amazon S3                     |
| **Data Profiling**   | AWS Glue DataBrew             |
| **Server**           | Amazon EC2 (VPC Server)       |
| **Data Collection**  | Clickstream data platform     |
| **ETL**              | AWS Glue                      |
| **Data Analysis**    | AWS Athena, SQL               |
| **Visualization**    | AWS ETL Dashboard             |
| **Security**         | AWS KMS, S3 Versioning        |
| **Monitoring**       | AWS CloudWatch                |

----

# 2. 🌐 AWS Data Analytic Platform for the City of Vancouver

---

## ✨ Project Description

Developing an AWS-based Data Analytic Platform (DAP) to enable the City of Vancouver to derive meaningful insights from its data. The platform supports data ingestion, profiling, cleaning, integration, and data wrangling, providing an efficient ETL pipeline to process large datasets securely. By leveraging advanced exploratory and descriptive analyses, this platform empowers the city to optimize decision-making processes for better governance and service delivery.

---

## 🏷️ Project Title

**AWS Data Analytic Platform for the City of Vancouver:** Harnessing Big Data for Informed Governance

---

## 🎯 Objective

To design and implement a scalable data analytics platform that converts raw municipal data into actionable insights. By performing descriptive and exploratory analyses, and data wrangling, the platform aims to uncover trends and correlations—enhancing operational efficiency and policy-making.

---

## 💡 Motivation

Modern cities rely on big data to improve governance. This project focuses on using AWS cloud services to process the City of Vancouver’s bid and contracts data efficiently. The insights derived from this platform help the city optimize its bid acceptance processes and identify critical factors influencing decisions.

---

## 📂 Datasets

### **1. Bid and Contract Dataset**

| **Field**             | **Description**                                      |
|-----------------------|------------------------------------------------------|
| **Bid_ID**            | Unique identifier for each bid                       |
| **Contract_Type**     | Type of contract (e.g., maintenance, development)    |
| **Bid_Amount**        | Proposed amount for the bid                          |
| **Bid_Status**        | Status of the bid (e.g., accepted, rejected)         |
| **Department**        | City department managing the bid                     |
| **Submission_Date**   | Date the bid was submitted                           |
| **Acceptance_Rate**   | Rate of bid acceptance for each type                 |
| **Notes**             | Additional remarks or observations                   |

---

## 🔬 Methodology

The project was structured into several phases, focusing on data ingestion, wrangling, cleaning, profiling, and exploratory analysis using AWS services. Below is a detailed breakdown:

### **1️⃣ Data Ingestion**

- **Objective**: Store raw municipal datasets securely and efficiently in AWS.
- **Tools Used**: **Amazon S3**, **AWS CLI**, **AWS Glue**.
- **Process**:
  1. Uploaded raw data (e.g., bids and contracts datasets) into Amazon S3 buckets.
  2. Configured S3 buckets for optimal organization with folders for raw, cleaned, and curated datasets.
  3. Applied **encryption** using AWS Key Management Service (KMS) to secure the data during and after upload.

---

### **2️⃣ Data Profiling, Wrangling, and Cleaning**

- **Objective**: Ensure data relevancy and accuracy by profiling, wrangling, and cleaning the data.
- **Tools Used**: **AWS Glue DataBrew**, **AWS Glue**.
- **Process**:
  1. **Data Profiling**:
      - Used AWS Glue DataBrew to profile data for completeness, missing values, and duplicates.
      - Generated summaries to visualize inconsistencies, null values, and data distributions.
  2. **Data Wrangling**:
      - Applied **categorical mapping** (e.g., "Yes/No" to "1/0") to prepare qualitative data for analysis.
      - Transformed column data types for compatibility with downstream processes.
      - Renamed columns for standardization and clarity.
      - Generated derived fields, such as `Average_Bid_Amount` and `Bid_Skewness`, to support deeper insights.
  3. **Data Cleaning**:
      - Removed duplicate rows and irrelevant columns.
      - Filtered out incomplete or invalid records.
      - Stored cleaned datasets in S3 buckets for further processing.

📷 **Screenshot Ideas**:
   - AWS Glue DataBrew profile summary (showing null values or data distributions).
   - Example of transformations or mappings applied in the DataBrew UI.

---

### **3️⃣ ETL Pipeline Design**

- **Objective**: Automate data extraction, transformation, and loading (ETL) for efficiency.
- **Tools Used**: **AWS Glue**, **AWS Glue Studio**.
- **Process**:
  1. Built ETL jobs using AWS Glue Studio:
      - Extracted raw S3 datasets.
      - Transformed the data (e.g., calculated aggregate metrics like acceptance rates).
  2. Scheduled the ETL pipeline to process new data uploads automatically.
  3. Stored transformed datasets in **Parquet format** for efficient querying and reduced storage costs.

📷 **Screenshot Ideas**:
   - ETL pipeline diagram in AWS Glue Studio.
   - Output configuration showing Parquet file format in S3.

---

### **4️⃣ Exploratory Analysis**

- **Objective**: Answer key research questions using SQL and curated datasets.
- **Tools Used**: **AWS Athena**, **Amazon S3**.
- **Process**:
  1. Created a database in AWS Athena from curated S3 datasets using AWS Glue crawlers.
  2. Ran SQL queries to analyze:
      - Correlations between bid amounts and acceptance rates.
      - Trends in contract types and department-specific performance.
  3. Exported query results for visualization.

📷 **Screenshot Ideas**:
   - AWS Athena interface showing SQL queries and query results.
   - Visualization of query outputs, such as acceptance rates or bid type distribution.

---

### **5️⃣ Data Security and Governance**

- **Objective**: Protect data integrity, confidentiality, and availability throughout the project.
- **Tools Used**: **AWS KMS**, **S3 Versioning**, **Replication Rules**.
- **Process**:
  1. Enabled **server-side encryption** for S3 buckets using AWS KMS.
  2. Applied **versioning** to S3 buckets to retain all modifications to datasets.
  3. Configured **replication rules** to create backups in a separate AWS region.
  4. Implemented lifecycle policies to transition infrequently accessed data to Glacier storage, reducing costs.

📷 **Screenshot Ideas**:
   - S3 bucket versioning configuration.
   - Lifecycle policy for Glacier transitions.
   - Replication rule setup for cross-region backups.

---

### **6️⃣ Data Observability and Cost Monitoring**

- **Objective**: Monitor resource utilization and costs to ensure project efficiency.
- **Tools Used**: **AWS CloudWatch**, **AWS CloudTrail**.
- **Process**:
  1. Created a **CloudWatch dashboard** to monitor:
      - S3 bucket storage usage.
      - ETL pipeline runtimes and costs.
  2. Set up **alerts** for cost thresholds to avoid overspending.
  3. Enabled **CloudTrail** to log all AWS API activity for governance.

📷 **Screenshot Ideas**:
   - CloudWatch dashboard showing resource usage metrics.
   - CloudTrail log summary highlighting API actions.

---

### **7️⃣ Exploratory Findings and Outputs**

- **Objective**: Summarize insights derived from analyses.
- **Process**:
  1. Stored curated datasets and SQL query results in S3 for reporting.
  2. Identified key trends, such as no direct correlation between bid amounts and acceptance rates, highlighting the influence of qualitative factors.
  3. Recommended future use of machine learning for deeper analyses.

📷 **Screenshot Ideas**:
   - Output datasets in S3 (final results in Parquet or CSV).
   - Graphs or tables illustrating insights from the SQL analysis.

---

## 📈 Insights & Findings

- **Bid Amount vs. Acceptance**: Analysis shows qualitative factors significantly influence bid acceptance beyond bid amounts alone.
- **Optimized Bid Processes**: Recommended further analyses incorporating machine learning for more precise insights.

---

## 🛠️ Tools & Technologies

| **Category**         | **Tool**                   |
|----------------------|---------------------------|
| **Storage**          | Amazon S3                 |
| **Data Profiling**   | AWS Glue DataBrew         |
| **ETL**              | AWS Glue                  |
| **Data Wrangling**   | AWS Glue DataBrew         |
| **Data Analysis**    | AWS Athena, SQL           |
| **Visualization**    | AWS CloudWatch Dashboards |
| **Security**         | AWS KMS, S3 Versioning    |

---

## 🏁 Conclusion

The AWS Data Analytic Platform for the City of Vancouver showcases how big data can be leveraged for municipal decision-making. With future enhancements, including machine learning models and global deployment strategies, the platform will further improve governance efficiency and sustainability.

----

# 3. 📊 Customer Credit Analysis and Marketing Segmentation

---

## ✨ Project Description

This project analyzes customer credit data for a bank using machine learning techniques to segment customers based on their credit card usage and propose targeted marketing strategies to increase credit card adoption and usage.

---

## 🏷️ Project Title

**Customer Credit Analysis and Marketing Segmentation:** A Machine Learning Approach to Understanding Credit Behavior

---

## 🎯 Objective

To analyze customer credit data, identify patterns in credit card usage, and segment customers using K-Means clustering. Based on these clusters, targeted marketing strategies were developed to increase credit card usage and enhance customer engagement.

---

## 💡 Motivation

This project aims to uncover insights from customer credit data to help the bank understand usage patterns and improve its marketing strategies. By segmenting customers, we can propose personalized actions that encourage greater credit card adoption and usage.

---

## 📂 Datasets

### **1. Customer Credit Data**

| **Field**             | **Description**                                         |
|-----------------------|---------------------------------------------------------|
| **Customer_ID**       | Unique identifier for each customer                     |
| **Age**               | Age of the customer                                     |
| **Credit_Limit**      | Credit limit of the customer                            |
| **Total_Transactions**| Total number of transactions in the last 12 months      |
| **Revolving_Balance** | The amount of revolving balance on the credit card      |
| **Utilization_Ratio** | Ratio of credit used to the total credit limit          |
| **Card_Category**     | Category of the credit card (e.g., Visa, MasterCard)    |

### **2. Processed Data**

| **Field**             | **Description**                                         |
|-----------------------|---------------------------------------------------------|
| **Util_Ratio**        | Ratio of credit used relative to the current bank's credit limit |
| **Change_Credit_Limit**| Change in credit utilization compared to the previous year |

### 🛠️ **Why These Datasets?**

- **Customer Credit Data**: Helps understand customer demographics and credit usage.
- **Processed Data**: Focuses on features that directly influence credit behavior and usage patterns.

---

## 🔬 Methodology

### 1️⃣ Data Profiling and Cleaning

1. **Data Preprocessing**:
   - Cleaned and imputed missing values for categorical and numerical features.
   - Normalized numerical features using standard scaling.
   - Removed irrelevant columns and handled outliers using the IQR method.

   ![Data Cleaning Screenshot](path/to/cleaning_screenshot.png)  
   *Screenshot: Before and after data cleaning process showing missing values and outlier handling.*

### 2️⃣ Exploratory Data Analysis (EDA)

2. **Correlation Analysis**:
   - Analyzed correlations between features to determine which ones were most influential in predicting customer behavior.

   ![Correlation Matrix](path/to/correlation_matrix.png)  
   *Screenshot: Correlation matrix showing relationships between key variables.*

3. **Feature Engineering**:
   - Created new features such as **Util_Ratio** (credit utilization ratio) and **Change_Credit_Limit** (change in utilization) to better understand customer behavior.

   ![Feature Engineering](path/to/feature_engineering.png)  
   *Screenshot: Example of feature engineering process, showing how new features were derived.*

### 3️⃣ Clustering and Marketing Strategy

4. **Clustering**:
   - Applied **K-Means clustering** to segment customers into four distinct groups based on their credit card usage patterns.

   ![Clustering Visualization](path/to/clustering_visualization.png)  
   *Screenshot: Clustering visualization showing how customers are grouped into different segments.*

5. **Marketing Strategy**:
   - Developed personalized marketing strategies for each cluster:
     - **Cluster 0**: Customers using credit cards from other banks—target with offers to switch to the bank’s credit card.
     - **Cluster 1**: Low credit card usage—encourage increased usage with incentives.
     - **Cluster 2 & 3**: High usage—focus on loyalty programs and premium offers.

   ![Marketing Strategy Overview](path/to/marketing_strategy.png)  
   *Screenshot: Overview of marketing strategies tailored for each customer segment.*

---

## 📈 Insights & Findings

- 🕒 **Usage Patterns**: Identified clusters of customers with varying credit card usage, enabling tailored marketing strategies.
- 📝 **Targeted Recommendations**: Suggested strategies for increasing credit card usage based on the needs of each cluster.

---

## 🏁 Conclusion

By segmenting customers based on their credit card usage, this project provides actionable insights into how the bank can target specific customer groups to increase credit card adoption and improve engagement. The proposed marketing strategies aim to enhance customer loyalty and optimize credit card usage.

---

## 🛠️ Tools & Technologies

| **Category**         | **Tool**                       |
|----------------------|--------------------------------|
| **Data Processing**   | Python, Pandas, NumPy         |
| **Machine Learning**  | Scikit-learn (K-Means)        |
| **Data Visualization**| Matplotlib, Seaborn           |
| **Feature Engineering**| Python, Pandas               |
| **Clustering**        | K-Means Algorithm             |

---

### **Try It Yourself**  
The code for this project is available on Google Colab. You can access and run it interactively using the link below:  
[Explore the Code on Google Colab](https://colab.research.google.com/drive/1tFhckznvRLKgXEcIAim9pJ2OoXjEMYHv?usp=sharing)

