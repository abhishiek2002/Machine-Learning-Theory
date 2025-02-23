<img src='./Images/Unsupervised Learning.png'>

# Unsupervised Learning

## What is Unsupervised Learning?

Unlike supervised learning, where we have labels (e.g., Spam or Not Spam, Cat or Dog), in unsupervised learning, we don't have labeled data.

👉 The goal is to find patterns, groups, or hidden structures in the data.

There are two main types of unsupervised learning:

    1️⃣ Clustering - Group similar data points together.
    2️⃣ Association Rule Mining - Find relationships between items.

## 1️⃣ K-Means Clustering

Used for grouping similar data points (e.g., segmenting customers, grouping similar articles).

### How it works:

    1️⃣ Choose the number of clusters (K)
    2️⃣ Randomly select K points as the initial cluster centers (centroids).
    3️⃣ Assign each data point to the nearest centroid.
    4️⃣ Update the centroids by calculating the mean of all points in a cluster.
    5️⃣ Repeat steps 3 and 4 until centroids stop changing.

📌 Example:

    If we have customer spending data, we can segment them into K = 3 groups:
        Cluster 1: High spenders
        Cluster 2: Medium spenders
        Cluster 3: Low spenders
    
Optimization:
    The Elbow Method is used to find the best value of K.
    Uses Euclidean Distance to measure similarity.

## 2️⃣ Hierarchical Clustering

Used when we don't know the number of clusters beforehand.

### How it Works:

    1️⃣ Start with each point as its own cluster.
    2️⃣ Merge the two closest clusters.
    3️⃣ Repeat until there's only one big cluster.

 