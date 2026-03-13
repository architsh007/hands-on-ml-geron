# Chapter 8 — Dimensionality Reduction

This chapter explores dimensionality reduction techniques from both **linear algebra** and **manifold learning** perspectives.  
The goal is to understand how high-dimensional data can be compressed while preserving important structure.

Dimensionality reduction is essential for:

- Visualization of high-dimensional data
- Reducing computational cost
- Removing redundant features
- Improving model generalization
- Understanding intrinsic structure of datasets

---

# Learning Objectives

After completing this chapter, the key concepts covered are:

- Variance maximization and PCA formulation
- Eigen decomposition and SVD interpretation
- Explained variance and reconstruction error
- Linear vs nonlinear dimensionality reduction
- Kernel trick for nonlinear projections
- Manifold learning and intrinsic dimensionality
- Visualization methods for high-dimensional data

---

# Notebooks Overview

## 1️⃣ PCA From Scratch
`01_pca_from_scratch.ipynb`

This notebook derives **Principal Component Analysis** step-by-step using linear algebra.

Topics covered:

- Covariance matrix computation
- Eigenvalue decomposition
- Projection onto principal components
- Reconstruction from reduced dimension
- SVD interpretation of PCA
- Explained variance analysis
- Scree plots and automatic component selection

Key insight:

PCA finds orthogonal directions that maximize variance and provides the **optimal linear dimensionality reduction**.

---

## 2️⃣ Kernel PCA (Nonlinear Projection)
`02_kernel_pca_nonlinear_projection.ipynb`

Kernel PCA extends PCA using the **kernel trick** to capture nonlinear relationships.

Topics covered:

- Failure of linear PCA on nonlinear data
- Kernel similarity matrix
- RBF kernel transformation
- Hyperparameter sensitivity (gamma)
- Visualization of nonlinear embeddings

Key insight:

Kernel PCA performs **linear PCA in a high-dimensional feature space**, enabling nonlinear dimensionality reduction.

---

## 3️⃣ Swiss Roll Manifold Analysis
`03_swiss_roll_kernel_pca.ipynb`

This notebook demonstrates how dimensionality reduction behaves on **nonlinear manifolds**.

Topics covered:

- Swiss roll dataset geometry
- Linear PCA limitations
- Kernel PCA unfolding behavior
- Gamma sensitivity
- Comparison with manifold learning methods

Key insight:

Nonlinear datasets lie on **low-dimensional manifolds embedded in high-dimensional space**.

---

## 4️⃣ t-SNE Visualization
`04_tsne_nonlinear_embedding.ipynb`

t-SNE is a nonlinear embedding technique designed for **visualizing high-dimensional data**.

Topics covered:

- Probability distributions in high-dimensional space
- KL divergence objective
- Student-t distribution in low dimension
- Perplexity as neighborhood size
- Visualization of manifold structure

Key insight:

t-SNE preserves **local similarity structure**, making it extremely effective for visualization.

---

## 5️⃣ Dimensionality Reduction Comparison
`05_dimensionality_reduction_comparison.ipynb`

This notebook compares several dimensionality reduction techniques on the same dataset.

Algorithms compared:

- PCA
- Kernel PCA
- Isomap
- t-SNE

Key insight:

Different dimensionality reduction algorithms preserve **different structural properties** of data.

| Method | Preserves | Strength | Limitation |
|------|------|------|------|
| PCA | Global variance | Fast and stable | Cannot capture nonlinear manifolds |
| Kernel PCA | Nonlinear similarity | Flexible mapping | High computational cost |
| Isomap | Geodesic distances | Recovers manifolds | Sensitive to neighborhood size |
| t-SNE | Local similarity | Excellent visualization | Distorts global distances |

---

# Key Takeaways

- High-dimensional datasets often have **low intrinsic dimensionality**.
- PCA provides optimal **linear dimensionality reduction**.
- Kernel methods allow PCA to capture **nonlinear structures**.
- Manifold learning methods approximate the **true geometry of data**.
- t-SNE is primarily a **visualization tool**, not a compression method.

Choosing the correct method depends on the task:

| Task | Recommended Method |
|-----|-----|
| Feature compression | PCA |
| Nonlinear structure | Kernel PCA |
| Manifold recovery | Isomap |
| Visualization | t-SNE |

---

# Tools Used

- Python
- NumPy
- Matplotlib
- Scikit-learn

---

# Next Chapter

The next chapter focuses on **Clustering and Unsupervised Learning**, including:

- K-Means
- MiniBatch K-Means
- DBSCAN
- Gaussian Mixture Models

These algorithms allow us to **discover structure in unlabeled datasets**.
