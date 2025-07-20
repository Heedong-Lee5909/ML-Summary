
# Supervised Learning with K-Nearest Neighbors (KNN)

## What is KNN?
- K-Nearest Neighbors (KNN) is a **supervised machine learning algorithm**.
- It is used for **classification and regression** tasks.
- KNN assumes that similar data points exist in close proximity.
- It labels new points based on the labels of their **nearest neighbors**.

## How KNN Works (Classification)
1. **Pick a value for K** (number of neighbors to consider).
2. **Calculate distance** from the query point to all training data points.
3. **Find K nearest neighbors** to the query point.
4. **Predict** the label by:
   - **Classification**: majority vote among the K neighbors.
   - **Regression**: average or median of target values.

## Example: Iris Dataset
- Dataset includes 3 iris species: *setosa*, *versicolor*, *virginica*.
- Features: sepal length/width, petal length/width.
- A scatterplot using sepal and petal lengths illustrates how KNN classifies new points.
- KNN achieved **93% accuracy** using K=3.

## Choosing Optimal K
- Use a labeled test dataset and try different values for K.
- Smaller K → **overfitting**.
- Larger K → **underfitting**.
- Test accuracy for various K values and select the one with the best result.

## Characteristics of KNN
- **Lazy learner**: stores training data; no explicit training phase.
- **Distance-based**: performance relies on feature scaling and distance metric.
- **Sensitive to irrelevant or dominant features**:
  - Use **feature scaling** (e.g., standardization).
  - Eliminate irrelevant or redundant features.

## Handling Skewed Class Distribution
- Basic majority voting can be biased toward dominant classes.
- Use **distance-weighted voting** to improve results.

## Best Practices
- **Scale features** to ensure fair distance calculations.
- **Remove irrelevant/redundant features** to reduce noise and improve accuracy.
- Use **domain knowledge** to select meaningful features.

## Summary
- KNN uses labeled data to predict outcomes for new data points.
- It is simple, interpretable, and effective when configured correctly.
- Key parameters: **value of K**, **distance metric**, and **feature selection**.

