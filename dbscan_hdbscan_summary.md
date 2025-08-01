
# DBSCAN and HDBSCAN Clustering Summary

## DBSCAN (Density-Based Spatial Clustering of Applications with Noise)

- **Definition**: DBSCAN is a density-based clustering algorithm that groups together points that are closely packed together, marking points that lie alone in low-density regions as outliers.
- **Key Parameters**:
  - `eps`: Radius of the neighborhood around a point.
  - `min_samples`: Minimum number of points required to form a dense region.
- **Point Types**:
  - **Core Point**: Has at least `min_samples` points within `eps` radius.
  - **Border Point**: Within the neighborhood of a core point but doesn't meet the density criteria.
  - **Noise Point**: Neither a core nor border point.
- **Algorithm Steps**:
  1. Choose `eps` and `min_samples`.
  2. For each unvisited point, determine if it’s a core point.
  3. Expand cluster from core points by including reachable neighbors.
  4. Label remaining points as noise.

- **Advantages**:
  - Identifies clusters of arbitrary shape and size.
  - No need to specify the number of clusters.
  - Handles noise well.

- **Limitations**:
  - Sensitive to parameter selection.
  - Difficulty in clustering data of varying densities.

---

## HDBSCAN (Hierarchical DBSCAN)

- **Definition**: An extension of DBSCAN that builds a hierarchy of clusters and extracts the most stable ones.
- **Key Features**:
  - Does not require `eps` to be set manually.
  - Works with varying density clusters.
  - Uses **cluster stability** to determine strong clusters.

- **Algorithm Overview**:
  1. Convert input space to a mutual reachability graph.
  2. Construct a minimum spanning tree (MST) of this graph.
  3. Condense the MST into a hierarchy of clusters.
  4. Extract the most stable clusters from the hierarchy.

- **Advantages over DBSCAN**:
  - More robust to varying densities.
  - Produces more coherent and detailed clustering.
  - Reduced sensitivity to noise and outliers.

---

## Comparison Example

- **DBSCAN**:
  - Found ~10 clusters in a dataset of Canadian museums using `min_samples=3`, `eps=0.15`.
  - Some high-density regions were lumped into a single cluster.

- **HDBSCAN**:
  - Automatically adjusted to local densities.
  - Found more distinct and coherent clusters.
  - Preserved detail in dense areas better than DBSCAN.

---

## Summary

| Feature                 | DBSCAN                                  | HDBSCAN                                 |
|------------------------|------------------------------------------|------------------------------------------|
| Cluster Shape          | Arbitrary                                | Arbitrary                                |
| Requires k             | No                                       | No                                       |
| Handles Noise          | Yes                                      | Yes (Better)                             |
| Handles Varying Density| Poorly                                   | Well                                     |
| Parameters             | `eps`, `min_samples`                     | `min_cluster_size` (no need for `eps`)   |
| Output                 | Flat clusters                            | Hierarchical with stability ranking      |

