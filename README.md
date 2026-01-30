
# Bank Customers Churn Prediction

## Introduction
In the highly competitive banking industry, customer retention is paramount. Customer churn—the phenomenon where clients discontinue their relationship with a bank—poses significant challenges, leading to revenue loss and increased acquisition costs. Understanding and predicting which customers are likely to leave enables banks to implement targeted retention strategies, thereby enhancing customer loyalty and profitability. 

This project focuses on developing a predictive analytics model to identify potential churners within a bank's customer base, utilizing a comprehensive dataset encompassing demographic, financial, and behavioral attributes.

## Problem Statement
The primary objective is to predict customer churn by analyzing various factors that influence a customer's decision to leave. By leveraging predictive analytics, we aim to build a model that accurately identifies customers at high risk of churning. 

This proactive approach allows:
* **CRM Teams:** To tailor personalized retention efforts.
* **Marketing Strategists:** To design targeted re-engagement campaigns.
* **Financial Analysts:** To forecast revenue impacts and allocate resources efficiently.

## Data Summary
The dataset is publicly available on Kaggle and is open-source through the **Apache 2.0 License**. It contains demographic, account, and financial data on 10,000 customers.

### Relevant Features:
* **Demographics:** Gender, Age, and Geographic Location.
* **Financial Data:** Credit Score, Balance, and Estimated Salary.
* **Account Features:** Number of Products, IsActiveMember, HasCrCard, and Tenure (years with the bank).
* **Target Variable:** `Exited` (1 if the customer churned, 0 if they stayed).

> **Note:** Administrative columns such as Row Number, Customer ID, and Surname were excluded from the modeling process as they do not contribute to predictive power.

## Predictive Modeling Approach
This is a **binary classification** problem. We analyze patterns and correlations in historical data to predict the likelihood of churn for current customers. The following models were evaluated:
1. Logistic Regression
2. K-Nearest Neighbors (KNN)
3. Decision Tree
4. Random Forest



---

## Conclusion & Results
The evaluation was based on **AUC (Area Under the Curve)** scores and **Recall** (the ability to identify all actual churners).

| Model | AUC Score | Recall (Churned) |
| :--- | :--- | :--- |
| **Random Forest** | **~83.83%** | 67% |
| **Decision Tree** | ~82.26% | **72%** |
| **Logistic Regression** | Lower | Lower |
| **KNN** | Lowest | Lowest |

### Key Takeaways:
* **Random Forest** provided the highest overall accuracy and AUC score.
* **Decision Tree** outperformed in **Recall**, capturing 72% of customers who actually churned, which is often more valuable for business retention efforts.
* **Recommendation:** Deploy both models in a test environment to monitor real-world performance. The model that consistently identifies at-risk customers with the highest accuracy over time should be fully integrated into the bank's daily operations.
