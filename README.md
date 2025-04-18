# 🌸 Iris Dataset Clustering Assignment

This project explores unsupervised clustering techniques on the classic **Iris dataset**, using a variety of preprocessing strategies and clustering algorithms. The performance is evaluated using three standard clustering metrics.

---

## 📁 Dataset

- **Source**: `sklearn.datasets.load_iris()`
- **Features**: 4 numerical features describing iris flower morphology
- **Target**: Species of iris (used only for reference, not for training)

---

## ⚙️ Clustering Algorithms Used

- **K-Means Clustering**
- **Agglomerative (Hierarchical) Clustering**
- **Mean Shift Clustering**

---

## 🔧 Preprocessing Techniques

- **Raw**: No transformation
- **Normalized**: StandardScaler
- **Transformed**: PowerTransformer
- **PCA**: Principal Component Analysis (2 components)
- **Norm + Trans**: StandardScaler + PowerTransformer
- **Norm + Trans + PCA**: StandardScaler + PowerTransformer + PCA (2D)

---

## 📏 Evaluation Metrics

- **Silhouette Score** *(higher is better)*
- **Calinski-Harabasz Index** *(higher is better)*
- **Davies-Bouldin Score** *(lower is better)*

---

## 📋 Results Summary

- Clustering was evaluated with 2, 3, 4, and 5 clusters for KMeans and Hierarchical.
- Mean Shift estimated the number of clusters automatically based on bandwidth.
- 
---

## 🏆 Best Clustering Configuration

| Method       | Preprocessing | Number of Clusters | Silhouette Score |
|--------------|---------------|--------------------|------------------|
| Hierarchical | PCA           | 2                  | **0.7112**       |

✅ This configuration yielded the most compact and well-separated clusters across all preprocessing and algorithm combinations.

---

## 📌 Observations

- **Hierarchical Clustering with PCA** performed best overall.
- **KMeans** was consistent but slightly behind in terms of silhouette score.
- **Mean Shift** showed variable performance depending on preprocessing and bandwidth.
- **Normalization + Transformation** helped in some cases, especially for Hierarchical Clustering.
- **PCA** helped reduce dimensionality and boost performance in select scenarios.

---

## 📈 Silhouette Score Visualization

The chart below shows the silhouette score for each preprocessing and clustering combination:

![Silhouette Score Comparison](silhouette_plot.png)

---

## ✅ Conclusion

Clustering performance is heavily influenced by the choice of preprocessing. In this case, **PCA combined with Hierarchical Clustering** gave the best separation of iris flower species based on silhouette score. This reinforces the importance of trying multiple combinations when working with real-world data.

