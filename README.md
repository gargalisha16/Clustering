# Clustering Assignment - Comparative Study

## Objective
To perform a comparative study of different clustering algorithms (KMeans, Hierarchical, MeanShift) using various pre-processing techniques and different numbers of clusters on multiple evaluation metrics.

---

## Dataset
- **Source**: UCI Machine Learning Repository
- **Dataset Used**: Iris Dataset (150 samples, 4 features)

---

## Clustering Algorithms Used
- **KMeans Clustering**
- **Agglomerative (Hierarchical) Clustering**
- **MeanShift Clustering**

---

## Pre-processing Techniques
- No Preprocessing
- Normalization (MinMaxScaler)
- Log Transform
- PCA (2 Components)
- Transform + Normalize
- Transform + Normalize + PCA

---

## Evaluation Metrics
- **Silhouette Score**
- **Calinski-Harabasz Index**
- **Davies-Bouldin Index**

---

## Sample Results

| Clustering | Preprocessing     | Clusters | Silhouette | Calinski-Harabasz | Davies-Bouldin |
|------------|-------------------|----------|------------|-------------------|----------------|
| KMeans     | none              | 3        | 0.74       | 3567              | 0.34           |
| KMeans     | normalize         | 3        | 0.69       | 6633              | 0.46           |
| Hierarchical | T+N+PCA         | 4        | 0.72       | 3589              | 0.57           |
| MeanShift  | pca               | NA       | 0.67       | 2028              | 0.60           |

> Full result table available in `clustering_results.csv`.

---

## Observations
- PCA sometimes reduces the performance due to dimensionality reduction.
- KMeans performed well with Normalization + PCA.
- Hierarchical methods were stable across preprocessing.
- MeanShift automatically chooses clusters, best when exact `k` is unknown.

---

## How to Run
1. Open `Clustering_Assignment.ipynb` in Google Colab
2. Run all cells
3. Outputs will be generated including result tables and charts

---

## ✅ Conclusion
This experiment highlights the importance of data preprocessing and proper evaluation in clustering tasks. Selection of preprocessing technique and algorithm can greatly influence performance.

