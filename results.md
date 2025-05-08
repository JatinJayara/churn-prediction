# Model Results: Customer Churn Prediction

**Model:** RandomForestClassifier  
Parameters: n_estimators=150, max_depth=9, class_weight='balanced'

## Main Metrics
- **Accuracy:** 76.4%
- **ROC-AUC:** 0.83

## Classification Report

| Class | Precision | Recall | F1-score | Support |
|-------|-----------|--------|----------|---------|
| 0     | 0.89      | 0.77   | 0.83     | 1033    |
| 1     | 0.54      | 0.75   | 0.63     | 374     |

**Overall accuracy:** 0.76 (1407 samples)  
**Macro avg:** Precision 0.72, Recall 0.76, F1-score 0.73  
**Weighted avg:** Precision 0.80, Recall 0.76, F1-score 0.77

## Key Insights
- **Contract type**, **tenure**, and **OnlineSecurity** are the most influential features in predicting churn (see SHAP summary plot).
- Customers with **month-to-month contracts** and **short tenure** are most likely to churn.
- Lack of **online security** or **tech support** increases churn risk.
- **Retention strategies:** Offer incentives for longer contracts, promote online security add-ons, and target high-risk segments identified by the model.

## Visualizations
See the README for SHAP summary, feature importance, ROC curve, and churn distribution plots.

---

*Results generated on: May 8, 2025*
