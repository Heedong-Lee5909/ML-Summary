
# K-Means Clustering Summary

K-Means is an iterative, centroid-based clustering algorithm that partitions a dataset into similar groups based on the distance between their centroids.

---

## 🎯 Goal of K-Means

The goal of K-Means is to **minimize within-cluster variance**, defined as:

$$
\sum_{i=1}^{K} \sum_{x \in C_i} \|x - \mu_i\|^2
$$

Where:

- $C_i$: Cluster $i$
- $\mu_i$: Centroid of cluster $i$
- $x$: A data point in cluster $C_i$

---

## 📌 Key Points

- **Initialization**: Randomly select `k` centroids.
- **Assignment Step**: Assign each point to the nearest centroid.
- **Update Step**: Recalculate centroids as the mean of the points assigned to them.
- **Repeat** until centroids do not change or max iterations are reached.

---

## ⚠️ Limitations

- Assumes convex clusters of similar size.
- Sensitive to outliers and noise.
- Poor performance with imbalanced cluster sizes.
- Optimal K must often be estimated using:
  - Elbow Method
  - Silhouette Analysis
  - Davies–Bouldin Index
