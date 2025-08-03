# Dimension Reduction Algorithms

## Overview

Dimension Reduction Algorithms reduce the number of dataset features without sacrificing critical dataset information. These algorithms simplify high-dimensional data, making it easier to analyze, visualize, and process in machine learning models.

## Main Algorithms

### 1. Principal Component Analysis (PCA)
- **Type**: Linear
- **Assumptions**: Features are linearly correlated
- **Functionality**:
  - Transforms features into a new set of uncorrelated variables (principal components)
  - Retains as much variance as possible
  - Principal components are orthogonal and ordered by the amount of variance they explain
- **Applications**: Noise reduction, simplification of feature space, visualization

### 2. T-Distributed Stochastic Neighbor Embedding (t-SNE)
- **Type**: Nonlinear
- **Functionality**:
  - Maps high-dimensional data to lower-dimensional space (2D/3D)
  - Preserves local structure (similarity of close points)
  - Less focus on global structure
- **Strengths**: Good for visualizing image and text data
- **Limitations**: 
  - Poor scalability
  - Sensitive to hyperparameters
  - Does not preserve distances well for distant points

### 3. Uniform Manifold Approximation and Projection (UMAP)
- **Type**: Nonlinear
- **Based on**: Manifold theory
- **Functionality**:
  - Builds a graph of high-dimensional data
  - Projects it into lower dimensions while preserving both local and global structure
- **Strengths**:
  - Better scalability than t-SNE
  - Often provides higher clustering performance

## Example: Comparison Using MakeBlobs Dataset

- 3D blobs are generated using Scikit-learn’s `make_blobs`.
- PCA:
  - Performs well due to linear correlation of data
  - Distinct separation of clusters
- t-SNE:
  - Identifies clusters accurately
  - Slight mix of overlapping cluster regions
- UMAP:
  - Preserves cluster structure similarly
  - Performs slightly better than t-SNE when overlap exists

## Summary

| Algorithm | Linear/Nonlinear | Focus                   | Pros                              | Cons                          |
|-----------|------------------|-------------------------|-----------------------------------|-------------------------------|
| PCA       | Linear           | Variance preservation   | Simple, fast, good on linear data | Not ideal for nonlinear data |
| t-SNE     | Nonlinear        | Local similarity        | Great for visualization           | Poor scalability, tuning req. |
| UMAP      | Nonlinear        | Local + global structure| Scales well, robust clustering    | Slightly complex to implement |

Dimensionality reduction is essential in handling high-dimensional data and is often used as a preprocessing step to improve model efficiency and performance.
