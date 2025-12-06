# E-Commerce Customer Churn Prediction

<!-- BADGE ROW -->
![Language](https://img.shields.io/badge/Language-Python-blue)
![Model](https://img.shields.io/badge/Model-XGBoost-brightgreen)
![Notebook](https://img.shields.io/badge/Format-Jupyter%20Notebook-orange)
![Category](https://img.shields.io/badge/Category-Machine%20Learning-yellow)
![Use Case](https://img.shields.io/badge/Use%20Case-Customer%20Churn-red)

This project predicts which e-commerce customers are likely to churn.  
The goal is to identify customers who may leave so the business can take early retention actions.

---

## Project Summary

The project prepares the dataset, encodes categorical fields, removes outliers, applies log transformation and trains an XGBoost model.  
The model is evaluated with cross validation and a confusion matrix.  
The notebook also uses an OLS model to show how features relate to churn probability.

---

## Workflow Overview

Raw Data
→ Data Cleaning
→ One-Hot Encoding
→ Remove Outliers
→ Log Transform
→ Train Test Split
→ XGBoost Model
→ Evaluation
→ Business Insights
---

## Business Problem

Churn is costly for e-commerce businesses.  
Most customers do not churn, which makes detection difficult.  
A predictive model helps target customers who may need attention.

---

## Objectives

1. Prepare and clean the dataset  
2. Build an XGBoost churn model  
3. Evaluate performance with cross validation  
4. Identify patterns linked to churn  
5. Provide business insights for retention

---

## Data Description

Dataset includes:

- Product price  
- Quantity  
- Total purchase amount  
- Age  
- Product category one-hot columns  
- Payment method one-hot columns  
- Gender one-hot columns  
- Churn label  

---

## Methodology

### 1. Data Cleaning
- Dropped unused ID and date fields  
- Removed unnecessary columns  
- Converted categorical fields with one-hot encoding  

### 2. Outlier Removal
IQR method applied to:

- Product price  
- Quantity  
- Total purchase amount  

### 3. Log Transformation
Log transformed numeric columns to reduce skew.

### 4. Modeling
- Train test split  
- XGBoost classifier  
- Five fold cross validation  
- Confusion matrix for evaluation  

### 5. OLS Model
Used OLS to understand how features relate to churn probability.

---

## Results

### XGBoost
- Mean cross validation accuracy: **0.7998**  
- Strong non-churn prediction  
- Limited churn detection due to imbalance  

### Confusion Matrix
- Many correct non-churn predictions  
- Few churn predictions  

---

## Business Impact

- Helps identify customers who may leave  
- Shows spending and category patterns tied to churn  
- Highlights churn risk by payment method  
- Supports targeted retention actions  
- Reduces broad marketing costs  

---

## How to Run

Install dependencies:
pip install pandas numpy scikit-learn xgboost seaborn matplotlib statsmodels



Steps:

1. Open `Churn_Prediction.ipynb`  
2. Place the dataset in the same directory  
3. Run cells in order  
4. Review the confusion matrix and OLS output  

---

## Key Insights

- Lower spending customers churn more  
- Lower quantity customers churn more  
- Cash payment users show higher churn  
- Product category affects churn likelihood  

---

## Limitations

- Dataset is imbalanced  
- Model predicts non-churn better than churn  
- More behavioral data is needed  
- Class balancing should be added in future work  

---

## Future Work

- Add class balancing (SMOTE or class weights)  
- Tune XGBoost hyperparameters  
- Add more customer behavior data  
- Compare with Logistic Regression and Random Forest  
- Build a churn monitoring dashboard  

---

## My Contribution

- Cleaned and prepared the data  
- One-hot encoded categorical fields  
- Removed outliers and applied log transformations  
- Trained and evaluated XGBoost  
- Ran OLS for feature interpretation  
- Prepared insights and project structure  

---
## Data Source & Contributors

Data Source: Kaggle

Contributors: Aanya Bhatia, Damario Abdalla, Lasya Lalpet Venkata, and Nilufar Dusnazarova
