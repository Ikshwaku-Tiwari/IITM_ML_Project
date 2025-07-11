# 📞 Bank Telemarketing Campaign - Customer Response Prediction

This project involves predictive modeling on data from direct marketing campaigns (phone calls) by a Portuguese banking institution. The goal is to **predict whether a client will subscribe to a term deposit** (`'yes'` or `'no'`) based on various demographic, contact, and campaign-related features.

---

## 📂 Dataset Overview

- `train.csv` – Training dataset
- `test.csv` – Testing dataset (without target labels)
- `sample_submission.csv` – Format for Kaggle-style submission

**Target Variable**: `y` (term deposit subscription: `yes` / `no`)

---

## 📊 Features Description

| Feature         | Description |
|----------------|-------------|
| `age`          | Age of the client |
| `job`          | Type of job (e.g. admin, blue-collar, student) |
| `marital`      | Marital status (married/divorced/single) |
| `education`    | Education level (primary/secondary/tertiary/unknown) |
| `default`      | Has credit in default? (yes/no) |
| `balance`      | Average yearly balance in euros |
| `housing`      | Has housing loan? (yes/no) |
| `loan`         | Has personal loan? (yes/no) |
| `contact`      | Type of communication used (telephone/cellular/unknown) |
| `duration`     | Last contact duration in seconds |
| `campaign`     | Number of contacts during this campaign |
| `pdays`        | Days since last contact from previous campaign (-1 = never contacted) |
| `previous`     | Number of contacts before this campaign |
| `poutcome`     | Outcome of the previous campaign (success/failure/other/unknown) |
| `last_contact_date` | Last contact date |

---

## 🧪 Approach

The pipeline consists of the following stages:

1. **Exploratory Data Analysis (EDA)**
   - Distribution plots, missing value handling
   - Target imbalance analysis

2. **Preprocessing**
   - Encoding categorical variables
   - Feature engineering and outlier treatment
   - Train/test split

3. **Model Training**
   - Logistic Regression
   - Random Forest
   - XGBoost
   - LightGBM
   - Hyperparameter tuning using `RandomizedSearchCV`

4. **Evaluation Metrics**
   - Accuracy
   - Precision, Recall, F1-score
   - ROC-AUC Curve
   - Confusion Matrix

---

## 📈 Results Summary

| Model           | Accuracy | F1-score | AUC-ROC |
|----------------|----------|----------|---------|
| Logistic Regression | 87% | 61% | 0.88 |
| Random Forest       | 90% | 67% | 0.91 |
| XGBoost             | 92% | 71% | 0.93 |

> 🔍 Final model selected: **XGBoost**, after tuning parameters like `max_depth`, `learning_rate`, `n_estimators`.
