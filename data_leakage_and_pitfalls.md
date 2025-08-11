# Data Leakage and Other Pitfalls

## 1. Definition of Data Leakage
- **Data Leakage**: Occurs when a model’s training data includes information not available in the real-world deployment scenario (e.g., future data).
- Leads to overly optimistic performance during training/validation but poor generalization in production.

---

## 2. Causes and Examples
- Using future data (e.g., tomorrow’s stock price to predict today’s).
- Feature engineering using the entire dataset (e.g., global averages).
- Improper handling of training/testing separation.

**Example**: Predicting house prices using average actual home prices from the entire dataset.

---

## 3. Data Snooping
- Happens when training data contains information from the test set.
- Often occurs during:
  - Improper feature engineering
  - Leakage in cross-validation folds
- **Mitigation**:
  - Keep training, validation, and test sets strictly separate.
  - Avoid computing statistics from the entire dataset.

---

## 4. Mitigation Strategies
- Avoid global averages or dataset-wide statistics.
- Properly separate training/validation/test sets.
- Ensure features are available at prediction time in real-world use.
- For **time-dependent data**, use time-series split rather than random split.
- During cross-validation:
  - Fit pipelines separately for each training fold.
  - Apply the fitted pipeline to its corresponding validation fold.

---

## 5. Time-Series Cross-Validation
- Use `TimeSeriesSplit` instead of `train_test_split` for temporal data.
- Data is split sequentially:
  - Past data → training set
  - Future data → validation set
- With each split:
  - Training set expands
  - Test set shrinks

---

## 6. Feature Importance Pitfalls
- **Redundant/Correlated Features**:
  - Shared importance values, making them appear less significant.
- **Scale Sensitivity**:
  - Algorithms like linear regression can be distorted if features are not scaled.
- **Correlation ≠ Causation**:
  - Important features may not be causal drivers.
- **Ignoring Interactions**:
  - Some models miss feature interactions (e.g., linear regression missing a multiplicative relationship).

**Example**:
- Two features individually have low importance for linear regression but their interaction is critical.
- Random forest may capture the interaction implicitly.

---

## 7. Other Modeling Pitfalls
- Using raw data without appropriate preprocessing.
- Choosing the wrong evaluation metric.
- Ignoring class imbalance (bias toward majority class).
- Blind reliance on AutoML without understanding the data/model.
- Performing “what-if” scenarios on non-causal data.

---

## 8. Key Takeaways
- **Data Leakage**:
  - Avoid contamination between train/validation/test sets.
  - Use proper cross-validation for time-series and hyperparameter tuning.
- **Feature Importance Pitfalls**:
  - Watch for redundancy, scaling issues, false causation assumptions, and missed interactions.
- **General Pitfalls**:
  - Misinterpreted metrics, unaddressed class imbalance, poor feature engineering, and incorrect assumptions in scenario modeling.

