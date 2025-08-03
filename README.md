# Lab 5: Clustering Techniques Using DBSCAN and Hierarchical Clustering
---

## Objective
To apply clustering techniques such as **Hierarchical Clustering** and **DBSCAN** on the Wine dataset. The aim is to explore unsupervised learning methods, visualize clusters using PCA, and evaluate clustering performance using various metrics.

---

## Dataset
- **Source**: `sklearn.datasets.load_wine()`
- **Features**: 13 chemical features of wine
- **Samples**: 178 total

---

## Preprocessing
- Standardized using `StandardScaler`
- PCA applied for dimensionality reduction to 2D for visualization

---

## Clustering Techniques

### Hierarchical Clustering
- Method: Agglomerative
- Linkage: Ward
- Clusters: 3

#### Visuals:
- PCA scatter plot colored by cluster
- Dendrogram for hierarchy visualization

---

### DBSCAN Clustering
- Parameters used: `eps=1.8`, `min_samples=5`
- Number of clusters (excluding noise): 7
- Cluster Labels Distribution:
  ```
  { -1: 118, 0: 16, 1: 15, 2: 6, 3: 5, 4: 5, 5: 8, 6: 5 }
  ```

---

## Evaluation Metrics for DBSCAN
> Only computed for non-noise data points:

- **Silhouette Score**: `0.25`
- **Homogeneity Score**: `1.00`
- **Completeness Score**: `0.56`

---

## Key Takeaways
- DBSCAN can identify noise/outliers, while hierarchical clustering forces all data into clusters.
- A balance between `eps` and `min_samples` is necessary for DBSCAN to work effectively.
- PCA greatly aids visualization but should not be used for actual clustering decisions.

---
