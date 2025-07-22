# K-Means Clustering – Summary

## 📌 What is K-Means?

K-Means is an **iterative, centroid-based clustering algorithm** used to partition a dataset into *k* distinct, non-overlapping clusters based on feature similarity.

- It minimizes the **within-cluster variance**.
- It assumes clusters are **convex**, **balanced in size**, and **spherical** in shape.

---

## ⚙️ How K-Means Works

1. **Initialization**: Choose the number of clusters \( k \) and randomly select initial centroids.
2. **Assignment Step**: Assign each data point to the nearest centroid using a distance metric (e.g., Euclidean).
3. **Update Step**: Recalculate centroids as the mean of the points in each cluster.
4. **Repeat** until centroids stabilize (convergence) or a maximum number of iterations is reached.

---

## 🎯 Objective Function

The goal of K-Means is to **minimize within-cluster variance**, defined as:

\[
\sum_{i=1}^{K} \sum_{x \in C_i} \| x - \mu_i \|^2
\]

Where:
- \( C_i \): Cluster \( i \)
- \( \mu_i \): Centroid of cluster \( i \)
- \( x \): A data point in cluster \( C_i \)

---

## 🧪 Behavior in Experiments

- Performs well with **well-separated clusters** of similar density and size.
- Performs poorly with:
  - **Imbalanced cluster sizes**
  - **Non-convex clusters**
  - **Outliers or noisy data**

---

## ❓ Choosing Optimal K

Techniques for estimating the best number of clusters:
- **Elbow Method**: Find the point where the within-cluster variance curve starts to flatten.
- **Silhouette Analysis**: Measure how similar a point is to its own cluster vs. other clusters.
- **Davies-Bouldin Index**: Lower values indicate better clustering.

---

## 📌 Summary

- K-Means is efficient and scalable.
- It’s sensitive to initialization and outliers.
- The number of clusters \( k \) must be pre-defined.
- Useful for applications like customer segmentation, image compression, and pattern discovery.
