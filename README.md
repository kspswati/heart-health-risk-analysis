# 🫀 AI-powered Heart Health Predictor

This project uses open-source health data to build an interpretable machine learning model that predicts whether a patient is at risk of heart disease. The goal is to empower early screening and improve patient decision-making through data-driven insights.

---

## 🎯 Project Objective

- Predict the presence of heart disease based on patient attributes such as age, cholesterol, blood pressure, and stress test results.
- Build an interpretable model using Logistic Regression with clearly explained feature impacts.
- Provide a business-ready analysis with performance metrics and visualization.

---

## 📂 Dataset

- **Source:** [UCI Heart Disease Dataset](https://archive.ics.uci.edu/ml/datasets/heart+Disease)
- **Samples:** 303 patients
- **Features:** Age, Sex, Chest Pain Type, Resting BP, Cholesterol, Fasting Blood Sugar, ECG Results, Max Heart Rate, Exercise-induced Angina, ST Depression, Slope, Number of Major Vessels, Thalassemia, Heart Disease Diagnosis

---

## 🔎 Exploratory Analysis

- Balanced target classes (~55% have heart disease)
- Strong correlations observed with:
  - Chest pain type (`cp`)
  - ST depression (`oldpeak`)
  - Exercise-induced angina (`exang`)
  - Max heart rate (`thalach`)

---

## 🧠 Model Used

- **Logistic Regression** (interpretable baseline)
- Evaluated with:
  - Accuracy, Precision, Recall, F1-Score
  - ROC-AUC Score

---

## ✅ Performance

| Metric       | Score |
|--------------|-------|
| Accuracy     | 0.85  |
| ROC-AUC      | 0.90  |
| F1-Score     | 0.87  |

---

## 📊 Feature Importance (via Coefficients)

Top predictors increasing risk:
- Chest pain type (cp_2, cp_3)
- Thalassemia (thal_3.0 = reversible defect)
- Male sex
- Exercise-induced angina

Top predictors lowering risk:
- Normal thalassemia (thal_2.0)
- Lower ST depression (`oldpeak`)
- Fewer major vessels (`ca`)

*See full chart in `outputs/` folder.*

---

## 🧱 Project Structure

├── data/ ← Dataset (CSV)
├── notebooks/ ← EDA + model building
├── outputs/ ← Charts and visualizations
├── README.md ← Project summary
├── requirements.txt ← Libraries used
└── .gitignore ← Housekeeping


---

## 📌 Key Takeaways

- Logistic regression can perform well on structured health data with proper preprocessing.
- Interpretable models are vital in healthcare for trust and accountability.
- Domain knowledge (e.g., chest pain types) is crucial for meaningful feature engineering.

---

## 💡 Future Work (Optional)

- Add SHAP-based local explanations
- Deploy via Streamlit as a self-serve diagnostic tool
- Add model retraining on larger datasets (e.g., MIMIC-IV)



