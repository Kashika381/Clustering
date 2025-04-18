📊 Comparative Study of Clustering Algorithms on the Iris Dataset
This project performs a comparative analysis of different clustering algorithms using various preprocessing techniques and cluster configurations. The goal is to evaluate how different methods perform on the Iris dataset using standard clustering evaluation metrics.

📁 Dataset
Name: Iris Dataset

Source: UCI Machine Learning Repository

Description: 150 samples with 4 numerical features and 3 actual classes (used only for reference).

🧪 Experiment Setup
✅ Preprocessing Techniques
StandardScaler (Z-score normalization)

MinMaxScaler (Feature scaling to [0, 1])

✅ Clustering Algorithms
KMeans

Agglomerative Clustering

DBSCAN

✅ Cluster Sizes Tested
k = 2, 3, 4, 5
(Note: DBSCAN does not use k)

✅ Evaluation Metrics
Silhouette Score (higher is better)

Calinski-Harabasz Index (higher is better)

Davies-Bouldin Index (lower is better)

📈 Visualizations
PCA was used to reduce features to 2D for plotting clusters

Scatter plots for each configuration

Bar charts comparing evaluation scores across methods

🔍 Results Summary (Sample)

Scaler	Algorithm	k	Clusters	Silhouette	Calinski-Harabasz	Davies-Bouldin
StandardScaler	KMeans	3	3	0.458	561.6	0.66
MinMaxScaler	Agglomerative	3	3	0.445	503.7	0.68
MinMaxScaler	DBSCAN	-	3	0.53	480.2	0.59
Best Silhouette Score: DBSCAN with MinMaxScaler
Best Calinski-Harabasz: KMeans with StandardScaler
Lowest Davies-Bouldin: DBSCAN with MinMaxScaler

📌 Conclusion
Preprocessing Matters: MinMaxScaler generally yielded better silhouette scores.

DBSCAN was effective for identifying natural cluster shapes and noise.

KMeans performed best in terms of cluster compactness (Calinski-Harabasz).

Agglomerative Clustering had solid but not best performance across the board.

💻 How to Run
Open the notebook in Google Colab

Run all cells

Visualize and interpret the output

Modify k-values or dataset for further experimentation

📂 Files
Clustering.ipynb: Main notebook

README.md: This file

🙌 Credits
Made using scikit-learn, matplotlib, seaborn, and pandas
