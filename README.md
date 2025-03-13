# Auto Insurance Fraud Detection using XGBoost and AWS SageMaker

## Overview
This project focuses on detecting fraudulent auto insurance claims using an XGBoost model deployed on AWS SageMaker. The goal was to handle imbalanced data effectively and improve fraud detection accuracy through feature engineering, bias evaluation, and hyperparameter tuning.

---

## Objective
- Develop an XGBoost model to classify fraudulent and legitimate claims.
- Optimize classification threshold based on precision-recall trade-offs.
- Improve fraud detection efficiency to reduce financial losses.

---

## Dataset
- **Train.csv** and **Test.csv**: Provided datasets containing customer and claims data.
- **Size**: ~100,000 rows (combined).

---

## Methodology
### 1. **Data Preprocessing and Feature Engineering**
- Handled missing values using imputation techniques.
- Encoded categorical variables using one-hot and label encoding.
- Scaled features to ensure consistency in model training.

### 2. **Model Training and Tuning**
- Trained an XGBoost model using AWS SageMaker.
- Tuned hyperparameters using SageMaker's built-in tuning capabilities:
  - Learning rate = 0.1
  - Maximum depth = 6
  - Subsample = 0.8
- Evaluated performance using AUC-PR (Area Under Precision-Recall Curve).

### 3. **Bias Evaluation and Adjustment**
- Used Amazon SageMaker Clarify to check for bias.
- Adjusted classification threshold to 0.35 to balance recall and precision.

### 4. **Model Lineage and Registry**
- Registered the model and its metadata in AWS SageMaker Model Registry.
- Tracked training artifacts and model lineage.

---

## Performance Metrics
- **AUC-PR**: 0.82 (balanced performance)
- **Precision**: 78.5%
- **Recall**: 81.2%
- **Optimal Classification Threshold**: 0.35

---

## Tools & Technologies
- **AWS SageMaker** – Model training, tuning, and deployment.
- **Amazon SageMaker Clarify** – Bias evaluation.
- **XGBoost** – Machine learning model.
- **Python** – (Pandas, NumPy, Scikit-learn, Matplotlib/Seaborn for EDA & visualization)
- **Jupyter Notebooks** – Modeling and analysis.

---

## Lessons Learned
- **Feature engineering** significantly impacts model performance.
- Precision-Recall curves are crucial for imbalanced classification problems.
- Threshold adjustment helps balance false positives and false negatives.

---

## Future Work
- Expand dataset to improve model generalization.
- Improve model interpretability using SHAP (SHapley Additive exPlanations).
- Deploy a real-time fraud detection pipeline using SageMaker.

---
