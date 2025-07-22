
# K-Means Clustering – Summary

## 📌 What is K-Means?

K-Means is an **iterative, centroid-based clustering algorithm** that partitions a dataset into *k* non-overlapping clusters, aiming to group similar data points together based on distance to cluster centroids.

---

## 🔁 How K-Means Works

1. **Initialize**:
   - Choose the number of clusters *k*.
   - Randomly initialize *k* centroids.

2. **Assign Points**:
   - Assign each data point to the nearest centroid based on a distance metric (typically Euclidean distance).

3. **Update Centroids**:
   - Recalculate centroids as the mean of all points in the cluster.

4. **Repeat**:
   - Continue steps 2 and 3 until centroids stabilize (no change) or max iterations are reached.

---

## 📉 Objective Function

The goal of K-Means is to **minimize within-cluster variance**, defined as:

$$
\sum_{i=1}^{K} \sum_{x \in C_i} \|x - \mu_i\|^2
$$

Where:

- \( C_i \): Cluster *i*  
- \( \mu_i \): Centroid of cluster *i*  
- \( x \): A data point in cluster \( C_i \)

---

## ⚠️ Limitations

- Sensitive to **initialization**
- Performs poorly on **imbalanced or non-convex clusters**
- Sensitive to **outliers**
- Assumes clusters are **spherical and similar in size**

---

## ✅ Strengths

- **Efficient** and **scalable** to large datasets
- Simple to implement
- Works well when clusters are clearly separated

---

## 🧠 Choosing K

Heuristics to select the optimal *k*:

- **Elbow Method**: Plot inertia vs. k and find the "elbow" point.
- **Silhouette Score**: Measures cohesion vs. separation.
- **Davies-Bouldin Index**: Measures average similarity of each cluster with its most similar one.

---

## 🧪 Visual Experiment Notes

- When blobs are well-separated (std = 1), K-Means performs well.
- When blobs overlap (std = 15), separation is poor.
- Too small or large *k* leads to under- or over-clustering.

