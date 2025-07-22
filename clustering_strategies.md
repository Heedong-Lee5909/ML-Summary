# Clustering Strategies in Real-World Applications

## What is Clustering?
Clustering is an unsupervised machine learning technique that groups data points based on similarity without requiring labeled output. It automatically organizes data into clusters to uncover hidden patterns or structures.

## Applications of Clustering
- **Customer Segmentation**: Identify customer groups with similar purchasing behavior for marketing purposes.
- **Image Segmentation**: Detect anomalies in medical imaging or identify image regions.
- **Anomaly Detection**: Detect outliers, fraud, or equipment malfunctions.
- **Feature Engineering**: Generate new features or reduce dimensionality.
- **Data Summarization & Compression**: Reduce dataset size by replacing points with cluster centers.
- **Market Segmentation**: Understand product preferences by user group.
- **Genetic Analysis**: Explore hierarchical relationships in biological datasets.

## Clustering vs Classification
| Clustering                | Classification                    |
|--------------------------|------------------------------------|
| Unsupervised             | Supervised                         |
| No labels required       | Requires labeled data              |
| Groups by similarity     | Predicts defined output classes    |

## Partition-Based Clustering
- **K-Means**:
  - Objective: Minimize intra-cluster variance.
  - Assigns data into *k* non-overlapping clusters.
  - Efficient and scalable.
  - Sensitive to initial centroid placement.

## Density-Based Clustering
- **DBSCAN (Density-Based Spatial Clustering of Applications with Noise)**:
  - Groups points closely packed together.
  - Effective for clusters of irregular shape.
  - Detects noise and outliers.
  - Does not require specifying number of clusters.

## Hierarchical Clustering
- Builds a tree (dendrogram) of nested clusters.
- Two major types:
  - **Agglomerative (Bottom-Up)**:
    - Start with each point as a single cluster.
    - Merge closest pairs iteratively based on a distance metric.
    - Visualized with a dendrogram.
  - **Divisive (Top-Down)**:
    - Start with one large cluster.
    - Recursively split into sub-clusters until a stopping criterion is met.

## Agglomerative Clustering Algorithm
1. Select distance metric (e.g., Euclidean distance).
2. Initialize each point as its own cluster.
3. Compute distance matrix.
4. Repeat:
   - Merge two closest clusters.
   - Update distance matrix.
   - Until stopping criterion is met (e.g., number of clusters).

## Divisive Clustering Algorithm
1. Begin with all points in one cluster.
2. Recursively split clusters based on dissimilarity.
3. Stop when minimum cluster size or structure is achieved.

## Visual Example (Canadian Cities)
- Distance matrix used to cluster cities like Toronto, Montreal, Ottawa, etc.
- Dendrogram tracks the merging process.
- Shows hierarchical relationships between cities based on proximity.

## Summary
- Clustering uncovers structure in unlabeled data.
- **K-Means** is best for compact, spherical clusters.
- **DBSCAN** handles arbitrary shapes and noise.
- **Hierarchical methods** are ideal for exploratory analysis and visualization.
