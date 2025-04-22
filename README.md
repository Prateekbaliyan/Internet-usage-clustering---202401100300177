# Internet-usage-clustering---202401100300177

This project applies unsupervised machine learning to segment internet users based on their daily usage behavior. By analyzing time spent online, site categories visited, and session frequency, we identify distinct user groups using KMeans clustering and evaluate cluster quality with multiple metrics.

---

## Overview

As internet usage grows in diversity, understanding user behavior is essential. This project uses clustering techniques to find patterns in an unlabeled dataset, providing insights useful for marketing, network optimization, user experience design, and digital wellbeing analysis.

---

## Dataset

The dataset contains anonymized records of user internet behavior with the following features:

| Feature                  | Description                                  |
|--------------------------|----------------------------------------------|
| `daily_usage_hours`      | Total hours spent online per day             |
| `site_categories_visited`| Number of distinct website categories visited|
| `sessions_per_day`       | Number of internet sessions per day          |

---

## Methodology

1. **Data Preprocessing**  
   - Checked for and handled missing values (none found).  
   - Used `StandardScaler` to normalize all features.

2. **Clustering**  
   - Applied KMeans clustering with `k = 3`.  
   - Reduced dimensionality to two principal components using PCA for visualization.

3. **Evaluation**  
   - Calculated Silhouette Score to assess cluster separation.  
   - Calculated Davies-Bouldin Index to measure cluster compactness.  
   - Employed the Elbow Method to determine the optimal number of clusters.

4. **Visualization**  
   - Created a 2D scatter plot of the clustered data (PCA-reduced).  
   - Plotted the Elbow Curve (inertia vs. number of clusters).

---

## Results

- **Silhouette Score:** 0.30  
- **Davies-Bouldin Index:** 1.16  
- Three distinct user clusters were identified, representing different usage patterns (low, moderate, and high usage).

---

## Visualizations

**Cluster Scatter Plot (PCA Reduced)**  
`path/to/cluster_plot.png`

**Elbow Method Plot**  
`path/to/elbow_plot.png`

---

## Technology

- Python 3  
- Pandas, NumPy  
- Scikit‑learn (KMeans, PCA, metrics)  
- Matplotlib, Seaborn

---

## References

- Scikit‑learn documentation: https://scikit-learn.org/  
- KMeans clustering (Wikipedia): https://en.wikipedia.org/wiki/K-means_clustering  
- Silhouette Score: https://scikit-learn.org/stable/modules/generated/sklearn.metrics.silhouette_score.html  
- Davies‑Bouldin Index: https://scikit-learn.org/stable/modules/generated/sklearn.metrics.davies_bouldin_score.html  

---
