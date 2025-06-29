#### MSCS_634_Lab_5
# MSCS 634 - Lab 5: Clustering with Hierarchical and DBSCAN

### 👤 Student Name:
Muluwork Geremew

### 🎓 Course:
MSCS 634 - Machine Learning

### 🧪 Lab Objective:
This lab explores unsupervised learning through two clustering techniques:
- **Hierarchical Clustering (Agglomerative)**
- **DBSCAN (Density-Based Spatial Clustering)**

We apply these methods to the **Wine dataset** from `sklearn.datasets`, focusing on:
- Visualizing clusters
- Evaluating clustering quality
- Comparing performance of both algorithms

---

### 📈 Methods & Metrics:

#### Algorithms Implemented:
- Agglomerative Hierarchical Clustering (with dendrogram)
- DBSCAN Clustering

#### Clustering Evaluation Metrics:
- **Silhouette Score**
- **Homogeneity Score**
- **Completeness Score**

---

### 📊 Summary of Results:

| Model              | Parameters Used            | Clusters | Noise Points | Silhouette | Homogeneity | Completeness |
|-------------------|----------------------------|----------|---------------|------------|-------------|---------------|
| Hierarchical       | `n_clusters = 3`           | 3        | N/A           | *N/A*      | *N/A*       | *N/A*         |
| DBSCAN             | `eps = 1.5`, `min_samples = 3` | 8    | 147           | 0.3311     | 1.0000      | 0.4319        |

---

### 🔍 Key Insights:

- **Hierarchical Clustering** formed meaningful clusters aligned with known wine classes, and the **dendrogram** provided strong visual guidance.
- **DBSCAN** required careful tuning and was highly sensitive to parameter values.
- DBSCAN’s ability to detect noise was both a strength and a challenge — in our case, it labeled **82% of data as noise**.
- Despite this, DBSCAN achieved **perfect homogeneity** in its identified clusters, though with low completeness.

---

### ⚠️ Challenges Faced:

- DBSCAN did not form valid clusters for most `eps`/`min_samples` combinations.
- Silhouette scoring was not possible for hierarchical clustering without additional cluster evaluation logic.
- Visualizing clusters in high-dimensional data required dimensionality reduction or feature slicing.

---

### 📂 Repository Contents:

- `Lab5_Clustering.ipynb`: Jupyter notebook with all steps, code, visualizations, and analysis.
- `README.md`: This summary file.

---

### 🚀 How to Run:

1. Clone this repository.
2. Open `Lab5_Clustering.ipynb` in Jupyter or VS Code.
3. Run all cells in order.

Make sure the following Python libraries are installed:

```bash
pip install scikit-learn pandas matplotlib numpy scipy
