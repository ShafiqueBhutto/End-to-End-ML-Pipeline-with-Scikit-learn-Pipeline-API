# End-to-End-ML-Pipeline-with-Scikit-learn-Pipeline-API

# Telco Customer Churn Prediction

This project implements a **production-ready machine learning pipeline** to predict customer churn for a telecom company. The pipeline handles **data preprocessing, model training, hyperparameter tuning, and model export**, making it reusable for future predictions.

---

## Table of Contents

- [Project Overview](#project-overview)  
- [Dataset](#dataset)  
- [Technologies & Libraries](#technologies--libraries)  
- [Project Workflow](#project-workflow)  
- [Getting Started](#getting-started)  
- [Usage](#usage)  
- [Results](#results)  
- [License](#license)  

---

## Project Overview

Customer churn is when customers stop using a company's service. Predicting churn is crucial for businesses to retain customers and reduce revenue loss.  

This project builds a **machine learning pipeline** that:

1. Preprocesses numeric and categorical data  
2. Trains models (Logistic Regression and Random Forest)  
3. Optimizes model hyperparameters using GridSearchCV  
4. Saves the complete pipeline using `joblib` for production use  

---

## Dataset

- **Name:** Telco Customer Churn Dataset  
- **Source:** [Kaggle](https://www.kaggle.com/blastchar/telco-customer-churn)  
- **Rows:** 7032  
- **Columns:** 21  
- **Target Column:** `Churn` (Yes / No)  

The dataset contains customer demographics, subscription info, billing data, and service usage.

---

## Technologies & Libraries

- Python 3.x  
- Pandas  
- NumPy  
- Scikit-learn  
  - Pipeline  
  - ColumnTransformer  
  - StandardScaler  
  - OneHotEncoder  
  - LogisticRegression  
  - RandomForestClassifier  
  - GridSearchCV  
- Joblib (for saving the pipeline)  
- Matplotlib & Seaborn (optional, for EDA)

---

## Project Workflow

1. **Data Cleaning & Exploration**  
   - Handle missing values  
   - Convert `TotalCharges` to numeric  
   - Drop irrelevant columns like `customerID`  

2. **Feature Separation**  
   - Identify numeric and categorical columns  
   - Target column: `Churn`  

3. **Train-Test Split**  
   - 80% training, 20% testing  
   - Stratified split to maintain class balance  

4. **Preprocessing Pipeline**  
   - StandardScaler for numeric features  
   - OneHotEncoder for categorical features  
   - Combined using `ColumnTransformer`  

5. **Model Pipeline**  
   - Logistic Regression  
   - Random Forest  
   - Combined with preprocessing in `Pipeline`  

6. **Hyperparameter Tuning**  
   - Use `GridSearchCV` to find the best Random Forest parameters  
   - Cross-validation used for reliable performance  

7. **Model Evaluation**  
   - Accuracy, Precision, Recall, F1-Score  

8. **Pipeline Export**  
   - Save the full pipeline using `joblib` as `churn_pipeline.pkl`  
   - Ready for production use  

---

## Getting Started

1. Clone the repository:

```bash
git clone <your-repo-url>
cd <repo-folder>

# Run the notebook or script
# Preprocessing + Model training + GridSearchCV
# Saves pipeline as churn_pipeline.pkl


Results
Accuracy: 0.7917
Precision (Churn=1): 0.63
Recall (Churn=1): 0.51
F1-score (Churn=1): 0.57



---

If you want, I can also make a **super-short GitHub-ready version with badges, dataset link, and Python version info**, which looks more professional and attractive for recruiters.  

Do you want me to do that too?
