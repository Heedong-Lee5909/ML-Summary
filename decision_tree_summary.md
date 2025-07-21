
# Decision Trees – Summary

## 📌 What is a Decision Tree?

- A **Decision Tree** is a flowchart-like structure used to classify data.
- **Internal nodes** represent tests on features.
- **Branches** represent the outcomes of tests.
- **Leaf nodes** represent the predicted class or value.

## 🛠️ How Decision Trees Work

- Trees are built recursively:
  - Start from the root with the training data.
  - At each node, choose the feature that best splits the data.
  - Continue until all leaves are pure, or stopping criteria are met.

### Stopping Criteria (Pre-pruning)

- Maximum tree depth reached.
- Minimum number of samples in a node.
- Minimum number of samples in a leaf.
- Maximum number of leaf nodes.
- Branches that don’t significantly improve accuracy may be pruned.

## 🌿 Pruning

- Simplifies the tree to avoid overfitting.
- Improves generalization and model interpretability.

## 🔍 Feature Selection and Splitting

- At each node, a splitting criterion determines the best feature:
  - **Entropy**: Measures disorder in a node (0 = pure, 1 = maximum impurity).
  - **Information Gain**: Reduction in entropy after a split.
  - **Gini Impurity**: Alternative to entropy for measuring split quality.

### Example

- Dataset: Patients treated with either **Drug A** or **Drug B**.
- Features: Age, Gender, Cholesterol, Blood Pressure.
- Goal: Predict which drug a new patient should receive based on features.
- Tree builds by testing features like age, then further splits using sex or cholesterol.
- Best splits lead to pure leaf nodes and maximum information gain.

## ✅ Advantages of Decision Trees

- Easy to understand and visualize.
- Feature importance is interpretable.
- No need for feature scaling.
- Works for both classification and regression tasks.

## 🧠 Summary

- Decision Trees classify data by testing features sequentially.
- They use splitting criteria like information gain or Gini impurity.
- Trees grow recursively until stopping criteria are met.
- Pruning improves performance and prevents overfitting.
