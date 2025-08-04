# Medical Appointment No-show Analysis & Predictive Modeling 🏥📊

## Overview
This project explores behavioral patterns behind missed medical appointments in Brazil using a real-world dataset. The goal: empower healthcare providers to anticipate no-shows and improve operational efficiency through machine learning.

## Key Insights
- 📅 **wait_time**, 👶 **Age**, and 📲 **SMS_received** are the strongest predictors of attendance.
- 🚸 Young children and elderly patients show distinctive no-show patterns.
- ✉️ Reminder systems (SMS) have a measurable impact on attendance rates.
- ⏳ Long scheduling delays (>100 days) drastically increase no-show likelihood.

## Modeling Pipeline
- **EDA & Feature Engineering**: Lifecycle-aware fields like `wait_time` were created to enhance prediction.
- **Model Comparison**: Logistic Regression, Random Forest, and XGBoost were benchmarked.
- **Class Imbalance Solution**: SMOTE improved recall across all models.
- **Threshold Tuning**: A sweet spot around 0.38 balanced clinic needs.
- **Model Explainability**: SHAP visualizations reveal age and wait time as top influencers.

## Performance Metrics (After SMOTE)
| Model                  | Accuracy | Precision | Recall | F1-Score | AUC  |
|------------------------|----------|-----------|--------|----------|------|
| XGBoost                | 61.93%   | 0.304     | **69.27%** | **0.42**     | **0.71** |
| Logistic Regression    | 67.36%   | 0.310     | 51.20% | 0.39     | 0.63 |
| Random Forest          | 66.68%   | 0.300     | 49.45% | 0.37     | 0.64 |

## Deployment Strategy
- ✅ Scoring system using XGBoost for real-time appointment triage.
- 📊 Power BI dashboard integration for visual analytics and outreach segmentation.
- 🔍 SHAP values used for transparent patient-level justification.
- 📆 Quarterly retraining to capture seasonal and behavioral shifts.

## Tools & Technologies
`Python`, `pandas`, `scikit-learn`, `XGBoost`, `SHAP`, `SMOTE`, `Seaborn`, `Matplotlib`, `Power BI`

---

## 💬 Author: Yetunde Olajumoke Olaleye  
Currently pursuing MSc in Business Analytics at the University of Greenwich, UK. Passionate about lifecycle-aware modeling, sentiment analysis, and using data for meaningful healthcare and retail solutions.

