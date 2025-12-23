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

Results:
| Model               | ROC-AUC  | Recall   | F1-Score |
| ------------------- | -------- | -------- | -------- |
| Logistic Regression | 0.84     | 0.33     | 0.13     |
| Random Forest       | 0.95     | **0.79** | 0.15     |
| **XGBoost**         | **0.97** | 0.73     | **0.29** |
XGBoost achieved the best balance between recall and precision, making it suitable for real-world fraud detection.

Visualizations:
  ROC Curve
  Confusion Matrix
  Correlation Heatmap

Key Learnings:
  Why accuracy is misleading in imbalanced datasets
  Importance of recall in fraud detection
  Trade-off between false positives and false negatives
  Ensemble models outperform linear models

Future Work:
  Real-time deployment
  Deep learning (LSTM / Autoencoders)
  Cost-sensitive learning


