# 🫀 Clinical Cardiovascular Disease Risk Prediction Pipeline

An end-to-end healthcare analytics and machine learning pipeline that processes clinical biometric records to predict a patient's risk of Cardiovascular Disease (CVD). This framework covers everything from physiological data auditing and anomaly removal to medical feature synthesis and an optimized gradient-boosted classification engine.

---

## 📊 Executive Summary & Key Results
* **Dataset Scale:** 70,000 raw patient observations.
* **Data Quality Engineering:** Designed custom filtering boundaries to isolate severe clinical logging errors (e.g., physiological impossibilities like systolic blood pressure exceeding 16,000 mmHg and negative diastolic metrics).
* **Clinical Feature Synthesis:** Engineered biologically grounded metrics including **Body Mass Index (BMI)** categories and categorized physiological **Blood Pressure Status** tiers based on global medical definitions (Normal, Elevated, Stage 1 & Stage 2 Hypertension).
* **Model Accuracy:** Evaluated via stratified splits to ensure validation stability, achieving an **AUC-ROC score of 0.8037** and a global accuracy of **74%**.

---

## 📈 Model Performance & Evaluation Metrics

The classification engine relies on an optimized **XGBoost Classifier**, maximizing predictive capabilities over traditional linear medical assessments.

### 1. Classification Report
```text
              precision    recall  f1-score   support

 Healthy (0)       0.72      0.79      0.75      6940
     CVD (1)       0.76      0.68      0.72      6793

    accuracy                           0.74     13733
   macro avg       0.74      0.73      0.73     13733
weighted avg       0.74      0.74      0.73     13733
