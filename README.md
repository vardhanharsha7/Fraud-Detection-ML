Fraud Detection in Online Payments Using Ensemble Learning

Online payment fraud is rare but extremely costly. The challenge lies in detecting fraudulent transactions from highly imbalanced data where fraud represents only 0.13% of total transactions.

Dataset:
Source: Kaggle (Online Payment Fraud Dataset)
Size: 6.3M transactions
Fraud rate: 0.13%
Key challenge: Severe class imbalance

Approach:
Data cleaning & validation
Feature engineering (balance differences, transaction type indicators)
Class imbalance handling:
  SMOTE
  Random undersampling
Models implemented:
  Logistic Regression (baseline)
  Random Forest
  XGBoost
  KNN
Hyperparameter tuning using Stratified K-Fold CV

Evaluation Metrics:
ROC-AUC (primary metric due to imbalance)
Precision, Recall, F1-Score
MCC for balanced evaluation
