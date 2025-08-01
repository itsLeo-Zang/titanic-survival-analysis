# 🚢 Titanic Survival Prediction Project

## 📌 Project Overview

This project aims to build a predictive machine learning model to estimate passenger survival in the Titanic disaster. The analysis follows the full data science pipeline: data cleaning, feature engineering, model training, and evaluation.

---

## 🧹 Data Preprocessing & Feature Engineering

- **Missing Values Handling:**
  - `Age`: Filled with median
  - `Embarked`: Filled with mode
  - Dropped `Cabin` column due to excessive missing data

- **Feature Transformations:**
  - `Sex` and `Embarked`: Converted to numeric using label encoding
  - Created new features:
    - `FamilySize` = `SibSp` + `Parch` + 1
    - `IsAlone`: Binary indicator if the passenger is alone
    - `Title`: Extracted from `Name` using regular expression

---

## 🧠 Model Training

- **Model Used:** Random Forest Classifier
- **Train/Test Split:** 80% training, 20% testing
- **Selected Features:**
  - `Pclass`, `Sex`, `Age`, `Fare`, `Embarked`, `FamilySize`, `IsAlone`, `Title`
- **Accuracy:** Achieved **83.24%** on test set

---

## 🔍 Evaluation

- Used confusion matrix to assess classification performance
- Model shows balanced prediction ability across survival classes


Confusion Matrix:

|             | Predicted: No       | Predicted: Yes      |
| ----------- | ------------------- | ------------------- |
| Actual: No  | 91 (True Negative)  | 14 (False Positive) |
| Actual: Yes | 16 (False Negative) | 58 (True Positive)  |
