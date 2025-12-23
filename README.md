# Fraud Detection in Online Payments Using Ensemble Learning

Online payment fraud is rare but extremely costly. The key challenge lies in detecting fraudulent transactions from **highly imbalanced data**, where fraud represents only **0.13%** of total transactions.

This project builds an end-to-end **machine learning pipeline** to identify fraudulent transactions using **ensemble learning techniques**.

---

##Dataset

- **Source:** Kaggle – Online Payment Fraud Dataset  
- **Size:** ~6.3 million transactions  
- **Fraud Rate:** 0.13%  
- **Key Challenge:** Severe class imbalance  

---

##Approach

### Data Preparation
- Data cleaning and validation
- Handling missing and inconsistent values

### Feature Engineering
- Balance difference features
- Transaction type indicators
- Derived numerical features to improve separability

### Handling Class Imbalance
- SMOTE (Synthetic Minority Over-sampling Technique)
- Random undersampling of majority class

### Models Implemented
- Logistic Regression (Baseline)
- Random Forest
- XGBoost
- K-Nearest Neighbors (KNN)

### Model Optimization
- Hyperparameter tuning using **Stratified K-Fold Cross Validation**
- Ensured consistent class distribution across folds

---

##Evaluation Metrics

Due to severe class imbalance, **accuracy was avoided** as a primary metric.

- **ROC-AUC** (Primary metric)
- **Precision**
- **Recall**
- **F1-Score**
- **Matthews Correlation Coefficient (MCC)** for balanced evaluation

---

##Results

| Model               | ROC-AUC | Recall | F1-Score |
|--------------------|---------|--------|----------|
| Logistic Regression | 0.84    | 0.33   | 0.13     |
| Random Forest       | 0.95    | **0.79** | 0.15     |
| **XGBoost**         | **0.97** | 0.73   | **0.29** |

**XGBoost achieved the best balance between recall and precision**, making it the most suitable model for real-world fraud detection scenarios.

---

##Visualizations

- ROC Curve comparison
- Confusion Matrix
- Correlation Heatmap

(Refer to the `images/` folder for visual outputs.)

---

##Key Learnings

- Accuracy is misleading in highly imbalanced datasets
- Recall is critical in fraud detection to minimize missed fraud cases
- Trade-off between false positives and false negatives must be carefully managed
- Ensemble models significantly outperform linear models in complex fraud patterns

---

##Future Work

- Real-time fraud detection system
- Deep learning approaches (LSTM, Autoencoders)
- Cost-sensitive learning methods
- Model deployment using REST APIs

---

##Technologies Used

- Python
- Pandas, NumPy
- Scikit-learn
- XGBoost
- Imbalanced-learn
- Matplotlib, Seaborn


