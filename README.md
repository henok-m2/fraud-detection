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

Model Performance
E-commerce Fraud Detection
Model	ROC-AUC	Avg Precision	F1-Score
Logistic Regression	0.85	0.78	0.72
Random Forest	0.92	0.85	0.79
Credit Card Fraud Detection
Model	ROC-AUC	Avg Precision	F1-Score
Logistic Regression	0.89	0.82	0.68
Random Forest	0.95	0.90	0.81
🔍 Key Findings
🛒 E-commerce Fraud Patterns
Time-based risks: Transactions within 2 hours of signup (5× higher fraud risk)

Nocturnal activity: Night transactions (2-5 AM) show 3× baseline risk

Velocity patterns: High transaction frequency (>3/hour) indicates fraud

Geographical insights: Non-US transactions have elevated fraud rates

💳 Credit Card Fraud Indicators
PCA components: V14 (low values) and V4 (high values) are strongest indicators

Amount anomalies: Large transactions with unusual patterns

Timing anomalies: Transactions inconsistent with customer history

💼 Business Impact
Fraud detection rate: >85% (from baseline ~70%)

False positive rate: <2% (reduced from ~5%)

Response time: <2 seconds for real-time scoring

Annual savings: Estimated $2M+ in prevented fraud for medium-sized banks

🎯 Tasks Completed
✅ Task 1: Data Analysis & Preprocessing
Exploratory Data Analysis with comprehensive visualizations

Geolocation integration (IP to country mapping)

Feature engineering including time-based features

Class imbalance analysis and handling strategies

✅ Task 2: Model Building & Training
Logistic Regression baseline models

Random Forest advanced models

Performance evaluation with AUC-PR, F1-Score metrics

Cross-validation and hyperparameter tuning

✅ Task 3: Model Explainability
Feature importance analysis using SHAP and built-in methods

Individual prediction case studies (TP, FP, FN)

Fraud driver identification

Actionable business recommendations

📁 File Descriptions
Notebooks (notebooks/)
File	Description	Run Time
01_eda_fraud_data.ipynb	E-commerce data exploration	5 min
02_eda_creditcard.ipynb	Credit card data analysis	3 min
03_feature_engineering.ipynb	Feature creation & preprocessing	2 min
04_modeling.ipynb	Model training & evaluation	10 min
05_model_explainability.ipynb	Model interpretation & insights	7 min
Generated Outputs
data/processed/: Cleaned datasets and engineered features

models/: Trained model artifacts (.pkl files)

results/: Performance metrics and visualizations

📊 Results & Insights
Top Fraud Indicators Identified
Transaction recency: Time since account creation

Behavioral anomalies: Unusual transaction patterns

Geographical mismatches: IP location vs billing address

Device fingerprints: Browser and device combinations

Amount patterns: Unusual transaction values

Business Recommendations
Immediate (0-3 months): Implement time-based risk scoring

Short-term (3-6 months): Deploy transaction velocity monitoring

Long-term (6-12 months): Develop customer behavioral baselines

👥 Author
Henok Mulugeta

10 Academy - Challenge Framework

🙏 Acknowledgments
10 Academy for the comprehensive challenge

Kaggle for the fraud detection datasets

Open-source community for invaluable tools and libraries

📞 Contact & Links
GitHub: henok-m2/fraud-detection

Email: h3nokmulugeta@gmial.com

🎓 Learning Outcomes
End-to-end machine learning project implementation

Handling imbalanced datasets in fraud detection

Model interpretability and business communication

Production-ready code organization and documentation


