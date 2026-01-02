Telco Customer Churn: Data Cleaning & Preprocessing
📌 Project Overview
This project focuses on the initial data cleaning phase of the Telco Customer Churn dataset. The goal was to transform raw, messy data into a structured format ready for Exploratory Data Analysis (EDA) and Machine Learning.
🛠️ Key Cleaning Steps
1. Data Type Correction
The TotalCharges column was initially loaded as an object type (text) due to empty strings. I converted this to a numeric format to allow for mathematical calculations.
Action: Used pd.to_numeric with errors='coerce'.
2. Missing Value Imputation
Converting types created NaN values where empty strings existed. Since these records usually represented new customers with zero tenure, I filled them with 0.
Action: fillna(0) applied to TotalCharges.
3. Feature Selection
The customerID column is a unique identifier that provides no predictive power for machine learning models. I removed it to keep the model focused on patterns.
Action: Dropped the column using df.drop().
4. Categorical Standardization
To simplify the dataset, I consolidated redundant categories. For example, "No internet service" and "No phone service" were mapped simply to "No."
Action: Used .replace() across multiple columns to reduce noise.
5. Duplicate Removal
Ensured data integrity by removing any identical rows that might skew the analysis results.
Action: df.drop_duplicates().


**EDA REPORT**
**Telco Customer Churn Analysis 📊**
This project focuses on identifying the key drivers behind customer churn in a telecommunications company. By performing a deep Exploratory Data Analysis (EDA), we uncover why customers leave and provide actionable business recommendations to improve retention.

**🚀 Project Overview**
Customer churn is a major problem for service-based industries. In this analysis, we cleaned a dataset of 7,043 customers and used visualization techniques to understand the relationship between demographics, account information, and service usage on churn.

**🛠️ Tech Stack**
Language: Python

Libraries: Pandas, NumPy, Matplotlib, Seaborn

Environment: Jupyter Notebook / Google Colab

**🧹 Data Cleaning Highlights**
Before the analysis, the data underwent rigorous cleaning:

Converted TotalCharges to a numeric format.

Handled missing values (imputed with 0 for new customers).

Simplified categorical values (e.g., merging "No internet service" into "No").

Dropped irrelevant columns like customerID.

**📈 Key Insights from EDA**
**1. The Contract Danger Zone**
Customers on Month-to-month contracts are the most likely to churn. High-tenure customers on Two-year contracts are the most loyal.

**2. Price & Service Sensitivity**
Churn peaks significantly when Monthly Charges exceed $70.

Fiber Optic users have a higher churn rate than DSL users, suggesting possible service or pricing dissatisfaction in that segment.

**3. "Sticky" Services**
Value-added services like Tech Support and Online Security act as "anchors." Customers with these services are much less likely to leave.

**💡 Final Recommendations**
Incentivize Long-term Contracts: Offer discounts to move month-to-month users to annual plans.

Focus on the First Year: Retention efforts should be heaviest during the first 12 months, where churn probability is highest.

Service Bundling: Bundle Tech Support with high-cost Fiber Optic plans to increase customer "stickiness."
