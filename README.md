# Customer Churn Prediction

## Overview

This project predicts customer churn for a telecom company using supervised machine learning. It demonstrates a complete data science workflow: from data cleaning and feature engineering to model building, evaluation, and explainability. The goal is to help the company identify at-risk customers and design effective retention strategies.

---

## Problem Statement

Telecom companies lose significant revenue when customers leave (churn). Predicting which customers are likely to churn enables targeted retention campaigns and improved business outcomes.

---

## Dataset

- **Source:** [Telco Customer Churn Dataset (Kaggle)](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- **Size:** 7,043 rows, 21 features (demographics, contract details, services used)
- **Target Variable:** `Churn` (Yes/No)

---

## Workflow

1. **Data Cleaning & Preprocessing**
   - Removed rows with missing/invalid values in `TotalCharges`
   - Encoded categorical variables using LabelEncoder
   - Scaled features with StandardScaler

2. **Exploratory Data Analysis (EDA)**
   - Visualized churn distribution and feature relationships

3. **Model Building**
   - Trained a Random Forest Classifier with class balancing
   - Evaluated using accuracy, precision, recall, F1-score, and ROC-AUC

4. **Explainability**
   - Used SHAP to interpret feature importance and model predictions

---

## Results

- **Model:** RandomForestClassifier (n_estimators=150, max_depth=9, class_weight='balanced')
- **Accuracy:** 76.4%
- **ROC-AUC:** 0.83

**Classification Report:**
      precision    recall  f1-score   support

       0       0.89      0.77      0.83      1033
       1       0.54      0.75      0.63       374

accuracy                           0.76      1407


---

## Key Visualizations

- **SHAP Summary Plot:**  
  ![SHAP Summary](download-3.jpg)
  - *Contract type*, *tenure*, and *OnlineSecurity* are the most influential features in predicting churn.

- **Feature Importance Bar Chart:**  
  ![Feature Importance](download-2.jpg)

- **ROC Curve:**  
  ![ROC Curve](download-1.jpg)

- **Churn Distribution:**  
  ![Churn Distribution](download.jpg)

---

## Business Insights

- Customers with **month-to-month contracts** and **short tenure** are most likely to churn.
- Lack of **online security** or **tech support** increases churn risk.
- **Higher monthly charges** also correlate with greater churn probability.
- **Retention strategies:** Offer incentives for longer contracts, promote online security add-ons, and target high-risk segments identified by the model.

---

## How to Run

1. **Clone this Repository**
2. **Install Dependencies**
3. **Download Dataset**
- Download from [Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- Place `WA_Fn-UseC_-Telco-Customer-Churn.csv` in the project folder
4. **Run the Notebook**
- Open `churn_prediction.ipynb` in Jupyter or Colab
- Execute all cells

---

## Tech Stack

- Python 3.x
- pandas, numpy, matplotlib, seaborn
- scikit-learn, shap

---

## Academic Context

This project is part of my portfolio for graduate admissions  and demonstrates my ability to solve real-world business problems with data science.

---

## Contact

For questions or collaboration, connect on [LinkedIn](
https://www.linkedin.com/in/jatinjayara/) or email [jatinjayara1@gmail.com
].

---

*All code and results are open-source and reproducible.*


