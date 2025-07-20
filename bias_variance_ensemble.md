
# 🎯 Bias, Variance, and Ensemble Models – Summary

## 🎯 Bias and Variance

- **Bias** measures the accuracy of predictions.
  - Low bias → Predictions are close to true values.
  - High bias → Systematic errors, poor fit.

- **Variance** measures how predictions change with different training data.
  - Low variance → Model is stable.
  - High variance → Model is sensitive, overfits.

- To generalize well, models need:
  - Low bias and low variance.

## 🎯 Bias-Variance Tradeoff

- As **model complexity** increases:
  - Bias decreases.
  - Variance increases.

- **Underfitting**: High bias, low variance.
- **Overfitting**: Low bias, high variance.
- The goal is to find a balance where the total error is minimized.

## 🎯 Bagging (Bootstrap Aggregating)

- Combines predictions from multiple models trained on different bootstrap samples.
- Reduces **variance** without increasing bias too much.
- Example: **Random Forests**
  - Multiple shallow decision trees.
  - Trained in parallel.

## 🎯 Boosting

- Trains models sequentially.
- Each model corrects the errors of the previous one.
- Reduces **bias** while slightly increasing variance.
- Examples:
  - **AdaBoost**
  - **Gradient Boosting**
  - **XGBoost**

## 🎯 Summary Table

| Method    | Goal         | Learner Type | Training Style  |
|-----------|--------------|--------------|-----------------|
| Bagging   | Reduce Variance | High variance, low bias | Parallel         |
| Boosting  | Reduce Bias     | Low variance, high bias | Sequential       |
