# credit-card-default-prediction
Machine learning project predicting credit card default risk using Python, Gradient Boosting, Logistic Regression, and SHAP explainability.
# Credit Card Default Prediction

## Overview

This project predicts whether a credit card customer will default on their payment in the following month using machine learning techniques.

The objective is to help financial institutions identify high-risk customers early, reduce financial losses, and support better lending decisions.

## Business Problem

Credit card default represents a significant risk for banks and fintech companies. Traditional rule-based approaches may fail to capture complex patterns in customer behaviour.

This project uses machine learning to identify customers with a higher probability of default based on demographic information, credit limits, repayment history, bill statements, and payment behaviour.

## Dataset

**Dataset:** Default of Credit Card Clients (UCI Repository)

* 30,000 customer records
* Default rate: 22.12%
* Binary classification problem:

  * 1 = Default
  * 0 = No Default

### Features

* Demographics (Age, Sex, Education, Marital Status)
* Credit Limit
* Repayment History
* Bill Statements
* Previous Payments

## Data Preparation

### Cleaning

* Removed ID column
* Checked for missing values
* Applied one-hot encoding to categorical variables

### Feature Engineering

* Standardized numerical variables for Logistic Regression
* Preserved original scaling for Gradient Boosting
* Used Pipeline and ColumnTransformer to prevent data leakage

## Machine Learning Models

### Baseline Model

**Logistic Regression**

Chosen for its simplicity and interpretability.

### Primary Model

**Gradient Boosting**

Chosen because it captures nonlinear relationships and feature interactions common in financial risk prediction.

## Results

| Model               | ROC-AUC | Precision | Recall | F1 Score |
| ------------------- | ------- | --------- | ------ | -------- |
| Logistic Regression | 0.71    | 0.3677    | 0.6323 | 0.4649   |
| Gradient Boosting   | 0.78    | 0.4794    | 0.6134 | 0.5382   |

### Key Finding

Gradient Boosting outperformed Logistic Regression by improving ROC-AUC, Precision, and F1 Score while reducing false positives.

## Explainability

SHAP (SHapley Additive Explanations) was used to improve transparency and understand model behaviour.

Key risk drivers included:

* PAY_0 (Repayment Status)
* LIMIT_BAL
* Recent Payment Behaviour

The analysis showed that repayment delays were among the strongest indicators of future default risk.

## Tools & Technologies

* Python
* Pandas
* NumPy
* Scikit-Learn
* Gradient Boosting
* Logistic Regression
* SHAP
* Matplotlib

## Skills Demonstrated

* Machine Learning
* Classification Modelling
* Feature Engineering
* Model Evaluation
* Explainable AI (XAI)
* Business Analytics
* Data Preprocessing

## Author

Arissa Andrade Araujo Santos

Higher Diploma in Data Analytics – First Class Honours
