
# Regression Trees – Summary

## 🌳 What is a Regression Tree?

- A **Regression Tree** is similar to a Decision Tree but is used to predict **continuous values** instead of discrete classes.
- Target variable:
  - **Classification Tree**: Categorical (e.g., "Yes"/"No")
  - **Regression Tree**: Continuous (e.g., temperature, salary)

## 🔍 Key Differences Between Classification and Regression Trees

| Aspect                      | Classification Tree                  | Regression Tree                       |
|----------------------------|---------------------------------------|---------------------------------------|
| Target Variable            | Categorical                           | Continuous                            |
| Prediction Method          | Majority vote at leaf                 | Average (or median) of target values  |
| Split Criterion            | Entropy or Information Gain           | Mean Squared Error (MSE)              |
| Common Use Cases           | Spam detection, diagnosis             | Revenue prediction, temperature       |

## 🧠 How Regression Trees Work

1. **Recursive Splitting**:
   - Data is split repeatedly to reduce variance of the target values.
   - Nodes are split using a selected **threshold α** for a feature.

2. **Prediction at a Node**:
   - The prediction \( \hat{y} \) is the **mean** of target values \( y_i \) in the node.
   - Median may be used when data is skewed.

3. **Splitting Criterion**:
   - Based on **Mean Squared Error (MSE)**:
     \[
     	ext{MSE} = \frac{1}{n} \sum (y_i - \hat{y})^2
     \]
   - For each split:
     \[
     	ext{Weighted MSE} = \frac{n_L}{n} MSE_L + \frac{n_R}{n} MSE_R
     \]
   - Choose the split that **minimizes weighted MSE**.

4. **Handling Feature Types**:
   - **Binary Feature**: Directly split into two subsets.
   - **Multi-class Feature**: Use one-vs-one or one-vs-all strategy to generate binary splits.
   - **Continuous Feature**:
     - Sort values
     - Remove duplicates
     - Compute midpoints as candidate thresholds:
       \[
       \alpha_i = \frac{X_i + X_{i+1}}{2}
       \]

5. **Threshold Selection**:
   - Try all candidate thresholds (exhaustive search).
   - For large datasets: use **sparse sampling** to improve efficiency.

## ✅ Summary

- **Regression Trees** are used for predicting continuous outcomes.
- Unlike classification trees, they optimize splits using **MSE**.
- Leaf node prediction = average of target values.
- Appropriate threshold and feature selection reduces prediction variance.
- Efficient threshold sampling is important for large-scale data.

