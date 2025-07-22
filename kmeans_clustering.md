
# K-Means Clustering Summary

## What is K-Means Clustering?

K-Means is an **iterative, centroid-based clustering algorithm** used to partition a dataset into K distinct, non-overlapping clusters. It operates by minimizing **within-cluster variance** and maximizing dissimilarity between clusters. Each cluster has a **centroid**—the average of the data points in that cluster.

---

## How the K-Means Algorithm Works

1. **Initialization**:
   - Choose a value for K (number of clusters).
   - Randomly select K initial centroid positions (can be real points or randomly generated).

2. **Assignment Step**:
   - Compute distances from each data point to each centroid.
   - Assign each data point to the nearest centroid.

3. **Update Step**:
   - Recalculate the centroid of each cluster as the mean of its assigned points.

4. **Repeat**:
   - Continue iterating the assignment and update steps until the centroids stop moving (convergence) or a maximum number of iterations is reached.

---

## Behavior and Performance

- **Well-balanced clusters**: K-Means performs well when clusters are of similar size and shape (convex).
- **Imbalanced clusters**: Poor performance when clusters have unequal sizes or densities.
- **Outliers**: Sensitive to noise and outliers due to the variance-based objective.
- **Convergence**: Typically fast; however, quality depends on initialization.

---

## Visual Behavior Example

- Centroids gradually move with each iteration until stable.
- In imbalanced cases, smaller clusters can be absorbed by larger ones.
- K-Means assumes **convex** clusters—cannot handle complex shapes well.

---

## Mathematical Objective

K-Means seeks to minimize:

\[
\sum_{i=1}^{K} \sum_{x \in C_i} \|x - \mu_i\|^2
\]

Where:
- \( C_i \): Cluster i
- \( \mu_i \): Centroid of cluster i

---

## Choosing the Right K

1. **Visualization**: In low dimensions (2D/3D), scatter plots help determine separability.
2. **Heuristics for Choosing K**:
   - **Silhouette Analysis**: Measures cohesion vs separation.
   - **Elbow Method**: Plots total within-cluster variance against K.
   - **Davies-Bouldin Index**: Measures similarity between clusters.

---

## Summary

- K-Means is efficient and scalable.
- Performs best on clean, convex, balanced clusters.
- Poor with irregular, imbalanced, or noisy datasets.
- Choosing K appropriately is crucial for performance.
- Heuristics and visual inspection help determine K in practical use.

