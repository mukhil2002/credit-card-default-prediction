# Credit Card Default Prediction

## Overview
Machine learning project to predict credit card default 
for 30,000 Taiwanese customers using six months of payment 
history and demographic data.

Built as part of MSc Financial Technology — Big Data 
Management in Finance.

## Key Results
| Model | Test AUC | Precision | Recall | F1 |
|---|---|---|---|---|
| Logistic Regression | 0.6926 | 0.38 | 0.56 | 0.45 |
| Decision Tree | 0.7263 | 0.43 | 0.54 | 0.48 |
| **Random Forest ★** | **0.7686** | **0.51** | **0.53** | **0.52** |
| XGBoost | 0.7607 | 0.51 | 0.49 | 0.50 |
| Neural Network | 0.7696 | 0.59 | 0.43 | 0.50 |

**Recommended model: Random Forest**
- Identified 705 of 1,327 actual defaulters (53%)
- Protected estimated NT$94.5M in potential losses
- 2.08x more efficient than random selection

## Project Structure
- section1.ipynb — Data quality control and EDA
- section2_and_3.ipynb — Model development, SHAP analysis, financial impact, recommendations
- CreditDefault_Dashboard.html — Interactive dashboard
- DecisionTree_output.png — Decision tree visualisation

## Methods Used
- Data cleaning and undocumented category resolution
- Feature engineering (avg_delay, payment_ratio, utilisation)
- SMOTE for class imbalance (78/22 split)
- Five ML models: Logistic Regression, Decision Tree, 
  Random Forest, XGBoost, Neural Network
- SHAP explainability analysis
- Risk tier segmentation
- Threshold analysis and financial impact quantification

## Technologies
Python 3.13 | scikit-learn | XGBoost | TensorFlow | 
SHAP | pandas | matplotlib | seaborn

## Dataset
UCI Credit Card Default Dataset — Yeh & Lien (2009)
30,000 customers | Taiwan | April–September 2005
Dataset not included in this repo due to licensing.
Available at: https://archive.ics.uci.edu/dataset/350
