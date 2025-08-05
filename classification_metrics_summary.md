
# Classification Metrics and Evaluation Techniques

## Overview
This guide covers key classification evaluation concepts, including the train-test split technique and core metrics such as accuracy, confusion matrix, precision, recall, and F1 score.

---

## 1. Supervised Learning Evaluation
- Determines how well a machine learning model generalizes to unseen data.
- Essential during both training and testing phases.
- Compares model predictions with ground truth labels to assess performance.

---

## 2. Train-Test Split
- **Purpose**: Estimate how well models perform on new, unseen data.
- **Method**: Split dataset into two subsets:
  - **Training set**: 70–80% of data; used to train the model.
  - **Test set**: Remaining data; used to evaluate generalization.

---

## 3. Evaluation Metrics

### 3.1 Accuracy
- Definition: Ratio of correct predictions to total instances.
- Formula: `Accuracy = (TP + TN) / (TP + TN + FP + FN)`

### 3.2 Confusion Matrix
|               | Predicted: Positive | Predicted: Negative |
|---------------|---------------------|---------------------|
| Actual: Positive | True Positive (TP)   | False Negative (FN)  |
| Actual: Negative | False Positive (FP)  | True Negative (TN)   |

### 3.3 Precision
- Measures the proportion of correctly predicted positives.
- Formula: `Precision = TP / (TP + FP)`
- **Example Use Case**: Movie recommendation system.

### 3.4 Recall
- Measures the proportion of actual positives that were correctly identified.
- Formula: `Recall = TP / (TP + FN)`
- **Example Use Case**: Medical diagnostics (minimize false negatives).

### 3.5 F1 Score
- Harmonic mean of precision and recall.
- Formula: `F1 = 2 * (Precision * Recall) / (Precision + Recall)`
- **Use Case**: When both precision and recall are equally important.

---

## 4. Practical Example
- **Dataset**: Iris flower dataset using a K-Nearest Neighbors (KNN) classifier.
- **Results**:
  - Accuracy: 93%
  - Confusion matrix: Mostly correct predictions (diagonal dominance).
  - Evaluation performed per class: setosa, versicolor, virginica.
  - Setosa achieved perfect scores on all metrics.
  - Weighted average used to account for class support.

---

## 5. Summary
- Supervised evaluation ensures reliable performance on unseen data.
- Train-test split is crucial for robust model validation.
- Use multiple metrics (accuracy, precision, recall, F1) to get a full picture of model performance.
