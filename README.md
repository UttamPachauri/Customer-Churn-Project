# Customer Churn Prediction Using Machine Learning

> Identify at-risk customers early — and keep them.

---

## Overview

This project analyzes customer churn behavior using machine learning techniques. The goal is to predict which customers are likely to leave a service, and to segment them into meaningful groups so businesses can apply targeted retention strategies.

---

## Dataset

| Attribute | Detail |
|-----------|--------|
| Source | Telco Customer Churn Dataset |
| Records | 7,043 customers |
| Features | Demographics, account info, subscribed services, tenure, billing details |

---

## Project Workflow

### Phase 1 — Data Preparation
- **Cleaning:** Resolved missing values in `TotalCharges`, corrected data types, dropped irrelevant columns
- **Preprocessing:** Applied one-hot encoding to categorical variables to produce an ML-ready dataset

### Phase 2 — Modeling
- **Split:** 80% training / 20% test
- **Algorithm:** Random Forest Classifier
- **Imbalance Handling:** Balanced class weights to improve minority class (churners) recall

### Phase 3 — Optimization
- Hyperparameter tuning across:
  - Number of estimators (trees)
  - Maximum tree depth

### Phase 4 — Evaluation
- Accuracy Score
- Confusion Matrix
- Classification Report
- ROC-AUC Score

### Phase 5 — Feature Importance
- Ranked features by their contribution to churn prediction

### Phase 6 — Customer Segmentation
- Generated churn probabilities per customer
- Standardized features and applied **K-Means Clustering**
- Produced three actionable customer segments:

| Segment | Description |
|---------|-------------|
| 🟢 Budget Loyal Customers | Low spenders with strong retention |
| 🔴 High Risk New Customers | Recent sign-ups showing early churn signals |
| 🟡 Loyal Premium Customers | High-value, long-tenure customers |

---

## Tech Stack

`Python` · `Pandas` · `NumPy` · `Scikit-Learn` · `Matplotlib` · `Seaborn`

---

## Results

The Random Forest model successfully identified customers at risk of churn. K-Means clustering then grouped customers into three distinct segments, enabling businesses to design personalized retention strategies for each group.

---

## Roadmap

- [ ] XGBoost implementation for improved accuracy
- [ ] Advanced hyperparameter optimization (GridSearch / Optuna)
- [ ] Streamlit deployment for interactive use
- [ ] Real-time churn prediction pipeline
