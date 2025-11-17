# 📊 Banking Data EDA & Fraud Detection

## 📌 Project Overview

This project performs **Exploratory Data Analysis (EDA)** on banking
customer data to uncover **financial patterns**, **behavioral trends**,
and **fraud indicators**.
The dataset contains detailed information about customer income, credit
usage, loan history, and payment behavior---making it suitable for
credit risk analysis and fraud detection.

------------------------------------------------------------------------

## 📂 Dataset Summary

-   **Total Records:** 10,000
-   **Features:** 28
-   **File Size:** ~29.3 MB

### 🔑 Key Columns

  Column Name                Type      Description
  -------------------------- --------- --------------------------------
  ID                         int64     Unique transaction identifier
  Customer_ID                int64     Unique customer identifier
  Age                        float64   Customer's age
  Occupation                 object    Type of occupation
  Annual_Income              float64   Yearly income
  Num_Bank_Accounts          float64   Total active bank accounts
  Num_Credit_Card            float64   Number of credit cards
  Num_of_Loan                float64   Number of loans taken
  Delay_from_due_date        float64   Days of delay from due date
  Num_of_Delayed_Payment     float64   Total delayed payments
  Changed_Credit_Limit       float64   Number of credit limit changes
  Outstanding_Debt           float64   Current unpaid debt
  Credit_Utilization_Ratio   float64   Utilization percentage
  Credit_History_Age         float64   Age of credit history
  Payment_Behaviour          object    Customer payment behavior
  Credit_Score               object    High/Low/Standard

------------------------------------------------------------------------

## 🎯 Project Objectives

-   ✔️ Explore and validate dataset structure\
-   ✔️ Identify financial patterns and customer segments\
-   ✔️ Detect anomalies indicative of possible fraud\
-   ✔️ Build insights for risk prediction and fraud detection models

------------------------------------------------------------------------

## 🔍 Key Insights

-   **High-risk indicators:**
    -   Excessive delayed payments
    -   High outstanding debt
    -   Frequent credit limit changes
    -   Poor payment behavior
-   **Useful Categorical Features:** Occupation, Type_of_Loan,
    Credit_Mix, Credit_Score
-   **Potential Redundancies:**
    -   Annual_Income vs Monthly_Inhand_Salary
    -   Num_of_Loan vs Type_of_Loan
-   **Strong Predictors of Creditworthiness:** Credit History Age,
    Credit Utilization Ratio
-   **Customer Profiling:** Based on income, age, occupation, and debt
    patterns

------------------------------------------------------------------------

## 🛠️ Data Cleaning & Wrangling

Steps completed:

-   Removed **duplicate rows**
-   Identified and handled **missing values**
-   Dropped irrelevant identifiers (`Name`, `SSN`)
-   Standardized inconsistent rules (e.g., `NM → No` in
    Payment_of_Min_Amount)\
-   Converted necessary float columns to **integers**
-   Rounded monetary values to **2 decimal places**
-   Added new engineered features:
    -   **Income_per_Account = Annual_Income / Num_Bank_Accounts**
    -   **Credit_Score_Level = High/Low** (threshold 700)
-   Exported final version → `cleaned_data_final.csv`

------------------------------------------------------------------------

## 📈 Post-Cleaning Insights

-   Dataset is now **fully ready for analytics and modeling**
-   Clean categorical labels → improved consistency
-   Numeric columns aligned and standardized
-   Engineered features enhance **predictive modeling potential**
-   Data quality significantly improved for fraud risk models

------------------------------------------------------------------------

## 🚀 Next Steps

-   Generate detailed **EDA visualizations**
    -   Distribution plots
    -   Outlier detection
    -   Correlation heatmaps
-   Apply additional feature engineering
    -   Debt-to-Income Ratio
    -   Credit Efficiency Score
-   Train **fraud detection ML models**
    -   Logistic Regression
    -   Random Forest\
    -   XGBoost\
-   Deploy findings in an interactive **dashboard** for real-time
    monitoring

------------------------------------------------------------------------

## 📁 Repository Structure (Suggested)

    banking-fraud-eda
    │
    ├── data
    │   ├── raw_data.csv
    │   └── cleaned_data_final.csv
    │
    ├── notebooks
    │   ├── 01_data_cleaning.ipynb
    │   └── 02_EDA.ipynb
    │
    ├── src
    │   ├── preprocessing.py
    │   └── fraud_model.py
    │
    ├── README.md
    └── requirements.txt

------------------------------------------------------------------------

## ⭐ Conclusion

This project lays a complete foundation for financial **EDA**, **credit
risk evaluation**, and **fraud detection modeling**.
It provides a structured approach for understanding customer behavior
and identifying high-risk cases based on data-driven insights.
