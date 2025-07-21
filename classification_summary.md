# Classification – Summary

## 📌 Classification Overview

- **Classification** is a supervised machine learning method used to predict categorical labels for new data using a fully trained model.
- The labels are discrete values, and classification aims to match inputs to these predefined categories.

## 🛠️ Applications and Use Cases

- **Email filtering**, **speech-to-text**, **handwriting recognition**, **biometric identification**, **document classification**.
- **Churn prediction**: Predict if a customer will discontinue service.
- **Customer segmentation**: Predict the category a customer belongs to.
- **Ad campaign targeting**: Predict if a customer will respond.
- **Loan default prediction**: Use features like age, income, credit level to predict default risk.
- **Drug prescription**: Predict which medication a patient may respond to.

## 🤖 Classification Algorithms

- **Naive Bayes**
- **Logistic Regression**
- **Decision Trees**
- **K-Nearest Neighbors (KNN)**
- **Support Vector Machines (SVM)**
- **Neural Networks**

## 🔄 Multi-Class Classification

- **Binary classifiers** predict between two classes.
- **Multi-class classifiers** handle more than two classes directly or through strategies:

### One-vs-All (OvA)
- One classifier per class.
- Each classifier distinguishes one class from the rest.
- Total of *k* classifiers for *k* classes.
- Unclassified points may indicate outliers or noise.

### One-vs-One (OvO)
- One classifier per pair of classes.
- For *k* classes, total classifiers = *k(k-1)/2*.
- Final prediction via **voting** (majority or weighted confidence).
- Used when OvA is ambiguous or when more granularity is required.

## ✅ Summary

- Classification is a supervised ML approach for categorical prediction.
- Applied in diverse areas: finance, healthcare, marketing, etc.
- Binary classifiers can be extended for multi-class tasks.
- OvA and OvO strategies are common approaches for handling multiple classes.
