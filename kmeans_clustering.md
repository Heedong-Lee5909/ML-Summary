
# K-Means Clustering Summary

## What is K-Means?

K-Means is an **iterative**, **centroid-based** clustering algorithm that partitions a dataset into _k_ non-overlapping groups or clusters, based on the distance between data points and cluster centroids.

- It is a **partition-based** unsupervised learning algorithm.
- It works best when clusters are **convex**, **similar in size**, and **well-separated**.
- It is **efficient** and **scales well** to large datasets.

---

## How the K-Means Algorithm Works

### 1. Initialization
Choose the number of clusters, **K**, and randomly initialize **K centroids**.

### 2. Assignment
Assign each data point to the **nearest centroid** based on a distance metric (usually Euclidean).

### 3. Update
Update the centroid of each cluster as the **mean of all points** assigned to it.

### 4. Repeat
Repeat assignment and update steps until convergence:
- Centroids no longer move
- Or maximum iterations reached

---

## Objective Function

The goal of K-Means is to **minimize within-cluster variance**, defined as:

$$
\sum_{i=1}^{K} \sum_{x \in C_i} \|x - \mu_i\|^2
$$

Where:
- \( C_i \): Cluster i
- \( \mu_i \): Centroid of cluster i
- \( x \): A data point in cluster \( C_i \)

---

## Limitations of K-Means

- **Performs poorly on imbalanced clusters**
- **Assumes convex clusters**
- **Sensitive to outliers and noise**
- **Needs K to be specified beforehand**

---

## Determining the Optimal K

Choosing K is a challenge. Several techniques help determine a good value for K:

1. **Silhouette Score** – Measures cohesion vs separation.
2. **Elbow Method** – Plots within-cluster sum of squares vs K.
3. **Davies-Bouldin Index** – Measures cluster similarity.

---

## Summary

- K-Means partitions data into K groups with minimal intra-cluster distance.
- It is efficient but sensitive to initialization and scale.
- Finding optimal K and preprocessing (e.g., feature scaling) are critical for good performance.
