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
