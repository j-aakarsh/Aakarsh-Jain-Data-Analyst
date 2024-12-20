# Aakarsh Jain
# 👋 About Me  
![IMG_20180404_201505_Original](https://github.com/user-attachments/assets/91e25b75-cdc3-4988-a2d4-5cb970a3832e)

Hi! I'm a passionate **Data Analyst** and aspiring **Machine Learning Enthusiast** with a background in **Mechanical Engineering** and an MBA specializing in **AI applications**. I  thrive at the intersection of technology and innovation, driving **data-driven solutions** to real-world challenges, including **sustainability** and **renewable energy**. With hands-on experience in building **ETL pipelines**, applying **machine learning algorithms**, and implementing **advanced data analytics**, I'm constantly exploring how data can solve complex problems.
## 🔍 What I Do  
- 🧠 Built machine learning models, including a **KNN-based clustering model** for banking credit card data.  
- 🛠 Developed pipelines for **ETL processes** using **AWS Glue** for scalable data integration.  
- 📊 Designed interactive data visualizations for effective storytelling and decision-making.  
- 🌱 Advocating for sustainable and innovative research through data insights.  

## 👨‍💻 Let's Collaborate  
I'm always open to collaborating on projects related to **data engineering**, **machine learning**, and **renewable energy**. Let's create something impactful together!  

🌟 *"Exploring the infinite possibilities hidden in data!"*

## 📂 My Projects 

---

# 1. 🌐 AWS Data Analytic Platform for the City of Vancouver

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

Primary Source of Data:
![Primary data COV](https://github.com/user-attachments/assets/f41a4cd2-df01-47a3-ab24-9525531fe00d)


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


<img width="1470" alt="cov ingestion" src="https://github.com/user-attachments/assets/a867a0dd-cebf-4f22-ba5a-f4501bfc376c" />
![Ingestion cov 1](https://github.com/user-attachments/assets/9028f68b-6a6c-4e6b-a64f-99f66e68974d)
![KMS cov](https://github.com/user-attachments/assets/805c7723-4e4c-4c6a-8a42-17dfbbe50e6f)

---

### **2️⃣ Data Profiling, Wrangling, and Cleaning**

- **Objective**: Ensure data relevancy and accuracy by profiling, wrangling, and cleaning the data.
- **Tools Used**: **AWS Glue DataBrew**, **AWS Glue**.
- **Process**:
  1. **Data Profiling**:
      - Used AWS Glue DataBrew to profile data for completeness, missing values, and duplicates.
      - Generated summaries to visualize inconsistencies, null values, and data distributions.
        
<img width="1470" alt="cov profiling and cleaning drawio" src="https://github.com/user-attachments/assets/1819f4f8-91fd-4f9e-82b4-a1d3749b8a17" />
<img width="1469" alt="Profiling UCW" src="https://github.com/user-attachments/assets/f64df607-4fea-4ac1-bd93-a5e9ba1f3064" />


  2. **Data Wrangling**:
      - Applied **categorical mapping** (e.g., "Yes/No" to "1/0") to prepare qualitative data for analysis.
      - Transformed column data types for compatibility with downstream processes.
      - Renamed columns for standardization and clarity.
      - Generated derived fields, such as `Average_Bid_Amount` and `Bid_Skewness`, to support deeper insights.
  3. **Data Cleaning**:
      - Removed duplicate rows and irrelevant columns.
      - Filtered out incomplete or invalid records.
      - Stored cleaned datasets in S3 buckets for further processing.

![cleaning COV](https://github.com/user-attachments/assets/773f0691-b6b9-4fc8-966a-0c0b251590aa)


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

![ETL 1 COV](https://github.com/user-attachments/assets/4e6fdb4a-88ab-4d8a-9b73-ce4ea8502034)
![Exploratory cov](https://github.com/user-attachments/assets/04efd37c-1dfc-40ca-bf99-b29ab474f35a)
 


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

![catalog cov](https://github.com/user-attachments/assets/e8d5a57f-1d58-4fd0-b76d-0866a02d507e)
![Athena cov](https://github.com/user-attachments/assets/8185a0a5-c648-4859-a8c6-b7c0b19fb57c)



---

### **5️⃣ Data Security and Governance**

- **Objective**: Protect data integrity, confidentiality, and availability throughout the project.
- **Tools Used**: **AWS KMS**, **S3 Versioning**, **Replication Rules**.
- **Process**:
  1. Enabled **server-side encryption** for S3 buckets using AWS KMS.
  2. Applied **versioning** to S3 buckets to retain all modifications to datasets.
  3. Configured **replication rules** to create backups in a separate AWS region.
  4. Implemented lifecycle policies to transition infrequently accessed data to Glacier storage, reducing costs.
  5. Conducted Architect Analysis to identify potential threats.

![KMS cov](https://github.com/user-attachments/assets/f64a3689-c580-46f8-9727-9ee2b8ba83d2)
![Rules cov](https://github.com/user-attachments/assets/83ec6d79-7bcd-42c5-a861-108528d9f20f)
![Architect Cov](https://github.com/user-attachments/assets/5052e304-e2ea-4cf4-b864-39ef7557494c)


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
 
![dashboard cov](https://github.com/user-attachments/assets/7d54bbd4-6e41-431f-a120-acc51406edeb)



---

### **7️⃣ Exploratory Findings and Outputs**

- **Objective**: Summarize insights derived from analyses.
- **Process**:
  1. Stored curated datasets and SQL query results in S3 for reporting.
  2. Identified key trends, such as no direct correlation between bid amounts and acceptance rates, highlighting the influence of qualitative factors.
  3. Recommended future use of machine learning for deeper analyses.

![sql query 1 cov](https://github.com/user-attachments/assets/84fb864b-a224-4233-bc43-50b2adaab60f)


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

---

# 2. 📊 Analysis of University Canada West's Grade Appeal Process

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

<img width="1470" alt="drawio ucw" src="https://github.com/user-attachments/assets/b0b72a05-f3d8-4277-8ff4-5c483fb0133b" />  
<img width="1470" alt="Data Ingestion UCW" src="https://github.com/user-attachments/assets/7dae90d8-4b2a-4a8e-bb81-a391951b81cc" />
<img width="1470" alt="DynamoDB UCW" src="https://github.com/user-attachments/assets/4ad44a7b-07a9-4741-b2a1-b76c7b93c585" />

 
 
2. **Descriptive Statistics**:
   - Generate summary statistics for numerical features and frequency distributions for categorical features.


 <img width="1470" alt="Analysisng Click stram data UCW" src="https://github.com/user-attachments/assets/4ffe4b8e-99cd-4003-a5c4-7b11d064a466" />


### 2️⃣ Diagnostic Analysis

3. **Data Profiling & Cleaning**:
   - Remove irrelevant columns, replace missing values, and format dates.
   - Create an ETL pipeline using **AWS Glue** to join datasets.

<img width="1469" alt="Profiling UCW" src="https://github.com/user-attachments/assets/6bbcf541-1dca-4c88-8e3e-f526f988e612" />
<img width="1468" alt="quality ucw" src="https://github.com/user-attachments/assets/e3f7795b-b25b-4e98-a066-6095aa745a34" />





4. **Security Enhancements**:
   - Enable encryption using **AWS KMS**.
   - Implement **S3 bucket versioning** and backups with replication rules.
   - Apply lifecycle rules to optimize storage costs.
   - Use VPC endpoint to download data using the internet securely from a virtual server
  
<img width="1470" alt="KMS UCW" src="https://github.com/user-attachments/assets/8d4d163f-9878-453f-b529-d00ceb9c4eea" />
<img width="1470" alt="Backup Buckets" src="https://github.com/user-attachments/assets/48567860-9d92-4c8e-b419-3004977fe58a" />
<img width="1470" alt="Versioning UCW" src="https://github.com/user-attachments/assets/10a5bf0f-65d9-440d-85e6-db2bf6a3b552" />
<img width="1470" alt="1  Create endpoint" src="https://github.com/user-attachments/assets/e24c9354-74e9-4ce4-9066-1406e2c3cfe6" />
<img width="1470" alt="Lifecycle UCW" src="https://github.com/user-attachments/assets/0aaef994-0eff-4ab8-bc2f-728d235c4b56" />
<img width="1470" alt="2  Create a virtual machine UCW" src="https://github.com/user-attachments/assets/01d2be8c-04c0-45e4-8b10-0057eec1fac2" />



### 3️⃣ Exploratory Analysis

5. **Data Analysis & Visualization**:
   - Use **AWS Glue crawlers** to generate relational database tables.
   - Run SQL queries in **AWS Athena** to analyze form-filling time and appeal outcome patterns.
   - Visualize insights using **AWS ETL Dashboard**.

<img width="1470" alt="AWS Glue UCW" src="https://github.com/user-attachments/assets/91a05ba8-7652-4f5e-a4e9-c70393a719db" />
<img width="1470" alt="Catalog UCW" src="https://github.com/user-attachments/assets/26727640-b21d-468c-82e9-3db7332b33b4" />
<img width="1470" alt="Athena UCW" src="https://github.com/user-attachments/assets/20915a80-f376-4086-bf8c-860b46b70955" />



### 4️⃣ Monitoring & Alerts

6. **Monitoring Costs**:
   - Create a dashboard in **AWS CloudWatch** to monitor service usage and costs.
   - Set up alarms for cost threshold breaches.

<img width="1470" alt="Alarm UCW" src="https://github.com/user-attachments/assets/a30c649d-f1b6-41ed-b55d-1369b43a1679" />
<img width="1353" alt="dashboard ucw" src="https://github.com/user-attachments/assets/77dc59ae-2439-486c-9366-e8f03a78cbed" />


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

![profilini ml](https://github.com/user-attachments/assets/af4569c7-ac74-4b26-aedb-e29d6a0da900)
![outlier ml](https://github.com/user-attachments/assets/87f2b2ac-ca8f-4eab-b880-0b57be934227)


### 2️⃣ Exploratory Data Analysis (EDA)

2. **Correlation Analysis**:
   - Analyzed correlations between features to determine which ones were most influential in predicting customer behavior.
     
![correl ml](https://github.com/user-attachments/assets/080d418e-9743-4bf1-a414-21926596b1be)


3. **Feature Engineering**:
   - Created new features such as **Util_Ratio** (credit utilization ratio) and **Change_Credit_Limit** (change in utilization) to better understand customer behavior.

<img width="956" alt="feature ml" src="https://github.com/user-attachments/assets/4125f986-142d-46ae-b8a5-a4b2ea60d661" />

### 3️⃣ Clustering and Marketing Strategy

4. **Clustering**:
   - Applied **K-Means clustering** to segment customers into four distinct groups based on their credit card usage patterns.

<img width="408" alt="elbow ml" src="https://github.com/user-attachments/assets/b52018c7-514c-4a00-b08c-2e54c4354dc4" />
![cluster ml](https://github.com/user-attachments/assets/94a5126f-f393-45ee-ab89-78f8d801c25d)


  

6. **Marketing Strategy**:
   - Developed personalized marketing strategies for each cluster:
     - **Cluster 0**: Customers using credit cards from other banks—target with offers to switch to the bank’s credit card.
     - **Cluster 1**: Low credit card usage—encourage increased usage with incentives.
     - **Cluster 2 & 3**: High usage—focus on loyalty programs and premium offers.

| Feature                | Cluster 0       | Cluster 1       | Cluster 2       | Cluster 3       |
|------------------------|-----------------|-----------------|-----------------|-----------------|
| Length/volume          | 1778           | 3286           | 1343           | 2756           |
| Credit Limit           | ≈ 0 - 20K +    | ≈ 0 - 10k      | ≈ 0 - 8K       | ≈ 0 - 20K +    |
| Total_Trans_Amt        | Max 17500      | Max 17500      | Max 5000       | Max 9500       |
| Total_Ct_Chng_Q4_Q1    | ≈ 0.4 – 1.2    | ≈ 0.4 – 1.2    | 0.5 < <br> 1 > | 0.5 < <br> 1 > |
| Avg_Utilization_Ratio  | ≈ 0 – 0.4      | ≈ 0 – 0.5      | ≈ 0 - 1        | ≈ 0 - 1        |
| Util_Ratio             | ≈ 0 - 1.4      | ≈ 1 - 5        | ≈ 0 - 1.4      | ≈ 0 – 0.5      |
| change_Credit_Limit_utilization         | ≈ MAX 1        | ≈ MAX 5        | ≈ Max 1.2      | ≈ Max 0.3      |
| Priority               | 3              | 1              | 4              | 2              |


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
[Explore the Code on Google Colab](https://github.com/j-aakarsh/data-analyst/blob/28d7a21bad52991987a40072876f39f07ffdbb92/group_project.ipynb)

