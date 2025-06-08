# Project-16
# Title :Customer Churn Prediction

    ## Project Overview

Interconnect Telecom aims to **predict customer churn** to proactively retain clients by offering **promotional codes** and **customized service plans**. By leveraging client demographics, service usage, and payment data, we developed a machine learning pipeline to forecast churn with high accuracy.

---

## Business Objective

Forecast client churn to:

- Reduce customer attrition
- Enhance customer retention strategies
- Inform marketing campaigns with targeted offers

---

## Data Overview

The dataset includes:

- **Demographics**: Gender, senior citizen status, age
- **Service details**: Internet type, security, tech support, streaming
- **Contract & payment info**: Contract length, payment method, electronic billing
- **Customer status**: Churn flag (binary target)

All data was merged using `CustomerID`.

---


## Machine Learning Models & Results

| Model               | AUC-ROC | Accuracy  |
|--------------------|---------|-----------|
| LightGBM           | 0.9319  | 0.8965    |
| XGBoost            | 0.9299  | 0.8891    |
| CatBoost           | 0.9264  | 0.8845    |
| Decision Tree      | 0.8611  | 0.8191    |
| Random Forest      | 0.8567  | 0.8123    |
| Logistic Regression| 0.8308  | 0.7998    |

**Final Model:** LightGBM  
**AUC-ROC:** 0.932  
**Accuracy:** 89.65%

---

## Confusion Matrix (Test Set)

|               | Predicted No Churn | Predicted Churn |
|---------------|--------------------|-----------------|
| **Actual No** | TN = 1238          | FP = 53         |
| **Actual Yes**| FN = 129           | TP = 338        |

---

## Strategic Recommendations

- Promote **long-term contracts** through onboarding incentives
- Offer **bundled services** (Tech Support, Online Backup, etc.)
- Encourage **automatic payments**
- Monitor **early churners** in their first months

---

## Deployment

LightGBM model is ready for integration into customer support/CRM systems for **real-time churn scoring** and **retention action triggers**.

---

## Repository Structure

    ## Setup
    1. Clone the repository
    2. Install dependencies: `pip install -r requirements.txt`
    3. Run the app locally using: `streamlit run app.py`
