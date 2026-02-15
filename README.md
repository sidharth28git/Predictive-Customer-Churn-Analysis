# 📉 Predictive-Customer-Churn-Analysis

A machine learning project that predicts customer attrition in the telecommunications industry. This end-to-end pipeline analyzes customer demographics, services, and account information to identify key drivers of churn and forecast high-risk customers.

## 🚀 Project Overview

Customer retention is critical for profitability. This project builds a predictive model to classify customers as "Churn" or "No Churn" based on historical data.

* **Goal:** Predict customer churn with high accuracy to enable proactive retention strategies.
* **Best Model Performance:** **79.25% Accuracy** using a tuned **XGBoost Classifier**.
* **Key Insight:** **Contract Type** (Month-to-Month) and **Tenure** are the strongest predictors of customer churn.

## 🛠️ Tech Stack

* **Language:** Python 3.10+
* **Data Manipulation:** Pandas, NumPy
* **Visualization:** Seaborn, Matplotlib
* **Machine Learning:** Scikit-learn, XGBoost
* **Model Tuning:** GridSearchCV

## 📊 Key Features & Workflow

1.  **Exploratory Data Analysis (EDA):**
    * Visualized class imbalance (27% Churn vs. 73% Retention).
    * Identified correlation between high monthly charges and churn rates using Seaborn.
2.  **Data Preprocessing:**
    * Handled missing values in `TotalCharges`.
    * Performed **One-Hot Encoding** for categorical variables (e.g., Contract, PaymentMethod).
    * Applied **StandardScaler** to normalize numerical features like Tenure and Monthly Charges.
3.  **Model Building & Comparison:**
    * **Logistic Regression:** Established a baseline for interpretability.
    * **Random Forest:** Captured non-linear relationships.
    * **XGBoost (Final):** Optimized via **GridSearchCV** for maximum accuracy (79.25%).

## 📈 Results

| Model | Accuracy | Key Takeaway |
| :--- | :--- | :--- |
| **Logistic Regression** | ~78% | Good baseline, highly interpretable coefficients. |
| **Random Forest** | ~79% | Better at capturing complex patterns. |
| **XGBoost (Tuned)** | **79.25%** | Best overall performance; balanced precision/recall. |

## 🧠 Key Insights

The model identified the following as the top factors influencing churn:
1.  **Contract_Month-to-month:** Customers on monthly contracts are significantly more likely to leave.
2.  **Tenure:** Newer customers have a higher risk of churning; risk decreases as tenure increases.
3.  **InternetService_FiberOptic:** Customers with Fiber Optic service showed higher churn rates (likely due to price or service issues).

## 💻 How to Run

1.  Clone the repository:
    ```bash
    git clone [https://github.com/yourusername/telecom-churn-prediction.git](https://github.com/yourusername/telecom-churn-prediction.git)
    ```
2.  Install dependencies:
    ```bash
    pip install pandas numpy seaborn matplotlib scikit-learn xgboost
    ```
3.  Run the analysis script:
    ```bash
    python churn_analysis.py
    ```
