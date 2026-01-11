# 🛡️ Real-Time Fraud Detection System

A machine learning system designed to detect fraudulent transactions in highly imbalanced financial datasets. 

## 🚨 The Challenge: The Accuracy Paradox
In financial data, fraud accounts for <1% of transactions. A model that blindly predicts "Safe" achieves 99% accuracy but fails its primary purpose.
**This project optimizes for Recall (Sensitivity)** to ensure fraudulent transactions are flagged, even at the cost of slightly lower precision.

## 🛠 Tech Stack
* **Scikit-Learn:** Random Forest Classifier.
* **Imbalanced-Learn:** SMOTE (Synthetic Minority Over-sampling Technique) to generate synthetic fraud examples for training.
* **Seaborn:** Confusion Matrix visualization.

## 📊 Methodology
1.  **Data Simulation:** Generated a dataset with a 99:1 imbalance ratio.
2.  **Resampling:** Applied SMOTE to the training set (never the test set) to achieve a 50:50 class distribution.
3.  **Training:** Trained a Random Forest on the balanced data.
4.  **Evaluation:** Achieved high Recall (0.85+) and ROC-AUC scores, proving the model can distinguish subtle fraud patterns.

## 🚀 Usage
Run `fraud_detection.py`. The script includes a simulated "Live API" function `check_transaction()` that accepts raw feature vectors and returns a Risk Score.
