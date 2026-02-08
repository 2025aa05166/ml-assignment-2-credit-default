# Credit Card Default Prediction (M.Tech AIML Assignment 2)

## Problem statement
Predict whether a credit card client will default in the next month (binary classification).

## Dataset description
UCI Credit Card Default Clients dataset  
- 30,000 instances  
- 23 features + ID + target (dpnm)  
- Features include demographic, payment history, bill & payment amounts  
- Target: 1 = default, 0 = no default (imbalanced ~22% default)

## Models used

| ML Model Name       | Accuracy | AUC   | Precision | Recall | F1    | MCC   |
|---------------------|----------|-------|-----------|--------|-------|-------|
| Logistic Regression | 0.8088   | 0.7100| 0.6923    | 0.2442 | 0.3610| 0.3302|
| Decision Tree       | 0.7185   | 0.6055| 0.3731    | 0.4009 | 0.3865| 0.2044|
| KNN                 | 0.7948   | 0.7042| 0.5561    | 0.3587 | 0.4361| 0.3292|
| Naive Bayes         | 0.2903   | 0.7240| 0.2340    | 0.9714 | 0.3771| 0.1034|
| Random Forest       | 0.8105   | 0.7592| 0.6243    | 0.3595 | 0.4562| 0.3711|
| XGBoost             | 0.8093   | 0.7552| 0.6193    | 0.3580 | 0.4537| 0.3673|

## Observations
- Random Forest & XGBoost are the best performers.
- Naive Bayes catches almost all defaults (high recall) but has many false positives.
- Logistic Regression is conservative (high precision, low recall).
- Ensembles clearly outperform single models on this dataset.

## Streamlit App Features
- Upload test CSV
- Select any of the 6 models
- Shows accuracy, AUC, precision, recall, F1, MCC
- Displays confusion matrix
- Download predictions CSV