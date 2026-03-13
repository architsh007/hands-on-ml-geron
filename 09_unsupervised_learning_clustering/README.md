# Chapter 9 — Unsupervised Learning: Clustering

This chapter explores clustering algorithms used to discover structure in unlabeled data.  
Unlike supervised learning, clustering attempts to group data points based on similarity without predefined labels.

The goal of this chapter is to build strong intuition for how different clustering algorithms behave and when they should be used.

---

# Learning Objectives

By completing this chapter, the following concepts are demonstrated:

- Understanding centroid-based clustering
- Evaluating clustering quality
- Detecting clusters with arbitrary shapes
- Performing dimensionality-aware clustering
- Applying clustering to real applications (image compression)
- Understanding probabilistic clustering models

---

# Notebooks Overview

## 1. K-Means Clustering Intuition
`01_kmeans_clustering_intuition.ipynb`

Introduces the K-Means algorithm and explains how centroid-based clustering works.

Key concepts covered:

- Cluster centroids
- Iterative optimization
- Distance minimization
- Voronoi partitioning
- Cluster geometry assumptions

---

## 2. K-Means Cluster Diagnostics
`02_kmeans_cluster_diagnostics.ipynb`

Demonstrates techniques for evaluating clustering quality.

Topics covered:

- Elbow method
- Silhouette score
- Cluster separation
- Choosing optimal number of clusters

---

## 3. K-Means Image Compression
`03_kmeans_image_compression.ipynb`

Applies clustering to a real-world problem: **image compression**.

Key idea:

Pixels are treated as RGB vectors and clustered into a limited set of representative colors.

This reduces the number of colors in the image while preserving visual structure.

Concepts illustrated:

- Color quantization
- Vector clustering
- Lossy compression using machine learning

---

## 4. DBSCAN: Density-Based Clustering
`04_dbscan_density_clustering.ipynb`

Explores density-based clustering.

Unlike K-Means, DBSCAN can:

- discover clusters of arbitrary shape
- detect noise/outliers
- avoid specifying the number of clusters in advance

Key parameters:

- ε (epsilon): neighborhood radius
- min_samples: minimum density threshold

---

## 5. Gaussian Mixture Models (GMM)
`05_gaussian_mixture_models.ipynb`

Introduces probabilistic clustering using Gaussian mixture models.

GMM extends K-Means by allowing:

- elliptical clusters
- probabilistic cluster assignments
- uncertainty modeling

Concepts demonstrated:

- soft clustering
- covariance matrices
- expectation-maximization (EM) algorithm
- cluster probability estimation

---

# Algorithm Comparison

| Algorithm | Cluster Shape | Outlier Detection | Hard / Soft Clustering |
|-----------|--------------|------------------|-----------------------|
| K-Means | Spherical | No | Hard |
| DBSCAN | Arbitrary | Yes | Hard |
| Gaussian Mixture | Elliptical | No | Soft |

---

# Key Takeaways

- Clustering discovers hidden structure in unlabeled datasets.
- K-Means works best for well-separated spherical clusters.
- DBSCAN is effective for irregular cluster shapes and noisy datasets.
- Gaussian Mixture Models provide probabilistic clustering and flexible cluster shapes.
- Choosing the right clustering algorithm depends heavily on the data geometry.

---

# Tools Used

The notebooks in this chapter primarily use:

- Python
- NumPy
- Matplotlib
- Scikit-learn

---

# Skills Demonstrated

This chapter highlights the following machine learning skills:

- Unsupervised learning techniques
- Clustering algorithm implementation
- Cluster evaluation and diagnostics
- Visualization of high-dimensional structures
- Real-world application of clustering methods

