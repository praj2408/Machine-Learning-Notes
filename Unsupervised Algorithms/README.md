# K-Means Clustering
![](https://github.com/praj2408/Machine-Learning-Notes/blob/main/Unsupervised%20Algorithms/K%20means.jpg)
 
## How to choose k value:
 Deciding the value of k (the number of clusters) in K-means clustering is a crucial step because it directly impacts the quality and interpretability of the clustering results. Here are several methods to help determine an appropriate value for k:

1. **Elbow Method**:
   - The elbow method is a popular heuristic for determining k. It involves plotting the within-cluster sum of squares (WCSS) against the number of clusters k. WCSS measures the compactness of clusters. As k increases, WCSS decreases because each cluster tends to have fewer data points. However, the rate of decrease typically slows down after a certain point, forming an "elbow" in the plot. The point where the rate of decrease sharply decreases is often chosen as the optimal k.
   - While the elbow method is widely used, it's important to note that the elbow might not always be clearly defined, especially in complex datasets.

2. **Silhouette Score**:
   - The silhouette score measures how similar an object is to its own cluster (cohesion) compared to other clusters (separation). It ranges from -1 to 1, where a high silhouette score indicates that the object is well matched to its own cluster and poorly matched to neighboring clusters. 
   - You can compute the silhouette score for different values of k and choose the value that maximizes the average silhouette score across all data points. This approach ensures both compactness and separation of clusters.
   
3. **Gap Statistic**:
   - The gap statistic compares the WCSS of the K-means clustering solution with that of a reference distribution (e.g., randomly generated data). It measures the gap between the observed WCSS and the expected WCSS under the null hypothesis (no clustering structure).
   - The optimal k is the value that maximizes the gap statistic.
   
4. **Silhouette Plot and Cluster Visualization**:
   - Visual examination of cluster assignments and silhouette plots can provide insights into the quality of clustering for different values of k. Silhouette plots display a silhouette coefficient for each sample, indicating the quality of clustering. Visual inspection of cluster assignments and silhouette plots can help identify the optimal number of clusters.
![](https://scikit-learn.org/stable/_images/sphx_glr_plot_kmeans_silhouette_analysis_004.png)

5. **Domain Knowledge**:
   - Consider domain-specific knowledge when choosing  k. If there are natural groupings or if you have prior knowledge about the data, it can guide the selection of k. For example, in customer segmentation, the number of distinct customer segments might be known based on business requirements or market research.

6. **Incremental Evaluation**:
   - Sometimes, starting with a small value of k and incrementally increasing it can provide insights into the structure of the data. You can evaluate the stability and interpretability of clusters as k increases.

7. **Practical Considerations**:
   - Consider practical implications such as computational resources and the interpretability of results when choosing k. Very large values of k may lead to clusters that are too small to be meaningful or computationally expensive to process.

## Types of K-Means

1. **Standard K-means**:
   - This is the basic version of the K-means algorithm, also known as Lloyd's algorithm. It iteratively assigns data points to the nearest cluster centroid and updates the centroids based on the mean of the points assigned to each cluster. The process continues until convergence, typically when cluster assignments no longer change or the centroids stabilize.

2. **K-means++**:
   - K-means++ is an initialization technique for selecting initial cluster centroids to improve the convergence and quality of the final clustering solution. Instead of randomly choosing initial centroids, K-means++ selects them in a way that ensures they are spread out and representative of the data. This initialization can lead to faster convergence and better clustering results, particularly for high-dimensional or difficult datasets.

3. **Mini-batch K-means**:
   - Mini-batch K-means is a variation of K-means designed to handle large datasets more efficiently. Instead of using the entire dataset to update centroids in each iteration, mini-batch K-means randomly selects a subset of data points (mini-batch) and uses them to update centroids. This approach speeds up convergence and reduces memory requirements, making it suitable for large-scale datasets.

4. **Kernel K-means**:
   - Kernel K-means extends the basic K-means algorithm to handle non-linearly separable data by applying the kernel trick. Instead of operating directly on the original feature space, Kernel K-means maps the data into a higher-dimensional feature space using a kernel function (e.g., Gaussian, polynomial) and performs clustering in this transformed space. This allows it to find complex, non-linear clusters that standard K-means may struggle with.

5. **K-medoids (PAM)**:
   - K-medoids, also known as Partitioning Around Medoids (PAM), is an alternative clustering algorithm to K-means that uses representative points (medoids) instead of centroids. Medoids are actual data points in the dataset, unlike centroids, which are virtual points. K-medoids iteratively selects medoids and assigns each data point to the nearest medoid, aiming to minimize the total dissimilarity between data points and their assigned medoids.

6. **Fuzzy K-means**:
   - Fuzzy K-means generalizes the crisp (hard) clustering of standard K-means to fuzzy (soft) clustering, where data points can belong to multiple clusters with varying degrees of membership. Instead of assigning each data point to a single cluster, fuzzy K-means assigns membership probabilities indicating the likelihood of a point belonging to each cluster. This approach allows for more flexible clustering, particularly when data points exhibit ambiguity or overlap between clusters.



# DB-SCAN Clustering
![](https://github.com/praj2408/Machine-Learning-Notes/blob/main/Unsupervised%20Algorithms/DBSCAN.jpg)




