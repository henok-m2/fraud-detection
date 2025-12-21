# Fraud Detection System for E-commerce and Banking

## Project Overview
This project implements machine learning models to detect fraudulent transactions in both e-commerce and banking contexts. The system addresses class imbalance challenges and provides interpretable predictions using SHAP analysis.

## Business Problem
Financial institutions face significant losses from fraudulent transactions. The key challenge is balancing security (catching fraud) with user experience (avoiding false positives). This project develops models that optimize this trade-off.

## Datasets
1. **E-commerce Fraud Data**: Transaction data with user demographics, device info, and timestamps
2. **Credit Card Fraud Data**: Anonymized PCA-transformed features from bank transactions

## Key Features
- Geolocation analysis using IP addresses
- Time-based feature engineering
- SMOTE for handling class imbalance
- Multiple model comparison (Logistic Regression, Random Forest, XGBoost)
- SHAP-based model interpretability
- Business-ready recommendations

## Project Structure
fraud-detection/
├── data/
│ ├── raw/ # Original datasets
│ ├── processed/ # Cleaned and engineered data
│ └── notebooks/ # Jupyter notebooks for analysis
├── models/ # Saved model artifacts
├── src/ # Source code modules
├── tests/ # Unit tests
└── requirements.txt # Python dependencies
Technologies Used
Python 3.9+

Scikit-learn, XGBoost, LightGBM

SHAP for explainable AI

Pandas, NumPy for data processing

Matplotlib, Seaborn for visualization


### requirements.txt

pandas==2.0.3
numpy==1.24.3
scikit-learn==1.3.0
xgboost==1.7.6
lightgbm==4.0.0
shap==0.42.1
imbalanced-learn==0.11.0
matplotlib==3.7.2
seaborn==0.12.2
jupyter==1.0.0
ipython==8.14.0
joblib==1.3.1
