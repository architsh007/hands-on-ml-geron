# Chapter 6 — Decision Trees & Ensemble Methods

This chapter explores tree-based models and ensemble learning techniques from both theoretical and practical perspectives.

We begin with single decision trees and progressively build toward Random Forest and Gradient Boosting — two of the most powerful classical machine learning methods for structured/tabular data.

The focus is not just implementation, but deep understanding of:

- Bias–variance behavior
- Model stability
- Regularization
- Sequential vs parallel ensembles
- Practical engineering tradeoffs

---

## 📌 Learning Objectives

By the end of this chapter, we understand:

- How decision trees split data using impurity measures
- Why trees are high-variance models
- How tree depth controls bias–variance tradeoff
- Why bagging reduces variance
- How Random Forest achieves decorrelated averaging
- Why Gradient Boosting reduces bias
- How learning rate controls boosting stability
- When to use Random Forest vs Gradient Boosting

---

## 📓 Notebooks Overview

### 1️⃣ Decision Tree Classification

Core concepts of classification trees:

- Gini impurity
- Entropy
- Information gain
- Axis-aligned decision boundaries
- Greedy recursive partitioning
- Visualization of decision regions

**Key insight:**  
Decision trees approximate complex boundaries using rectangular partitions.

---

### 2️⃣ Decision Tree Regression

Understanding regression trees:

- MSE-based splitting
- Piecewise constant predictions
- Why trees cannot extrapolate
- Overfitting behavior in deep trees

**Key insight:**  
Regression trees predict the mean target value in each region, leading to step-like functions.

---

### 3️⃣ Tree Regularization & Overfitting

Controlling model complexity:

- `max_depth`
- `min_samples_split`
- `min_samples_leaf`
- `max_leaf_nodes`
- Bias–variance tradeoff in trees

**Key insight:**  
Deep trees have low bias but extremely high variance.

---

### 4️⃣ Random Forest

Reducing variance through ensemble averaging:

- Bootstrap sampling
- Feature randomness
- Tree decorrelation
- Out-of-Bag (OOB) error
- Feature importance

**Key insight:**  
Random Forest reduces variance while maintaining low bias by averaging many decorrelated deep trees.

**Strengths:**
- Robust to noise
- Minimal hyperparameter tuning
- Strong out-of-the-box performance

**Limitations:**
- Cannot extrapolate well
- Feature importance may be biased
- Larger memory footprint for many trees

---

### 5️⃣ Gradient Boosting

Reducing bias through sequential error correction:

- Residual fitting
- Learning rate
- Shallow weak learners
- Sequential model building
- Bias reduction vs variance reduction

**Key insight:**  
Each new tree corrects the errors of the previous ensemble.

**Strengths:**
- Very high predictive performance
- Strong on tabular datasets

**Limitations:**
- Sensitive to hyperparameters
- Higher risk of overfitting
- Slower training compared to Random Forest

---

## 🧠 Core Conceptual Comparisons

| Model | Primary Goal | Training Style | Main Risk |
|--------|-------------|---------------|-----------|
| Decision Tree | Fit data directly | Greedy | High variance |
| Random Forest | Reduce variance | Parallel | Moderate bias |
| Gradient Boosting | Reduce bias | Sequential | Overfitting |

---

## 🔬 Bias–Variance Perspective

- Deep tree → Low bias, high variance  
- Bagging (Random Forest) → Reduces variance  
- Boosting → Reduces bias  

Understanding this distinction is fundamental to ensemble learning.

---

## ⚙️ Engineering Tradeoffs

### When to Use Random Forest
- Medium-sized dataset
- Moderate noise
- Minimal tuning required
- Stable performance needed

### When to Use Gradient Boosting
- High predictive accuracy required
- Willing to tune hyperparameters
- Clean or moderately noisy data
- Structured/tabular datasets

---

## 🛠 Tools Used

- Python
- NumPy
- Matplotlib
- Scikit-learn

---

## 📈 Why This Chapter Matters

Tree-based ensembles are:

- State-of-the-art for tabular data
- Widely used in industry
- Foundation for XGBoost, LightGBM, CatBoost
- Frequently asked in interviews

Mastering this chapter builds strong intuition about:

- Bias–variance tradeoff
- Model stability
- Ensemble averaging
- Sequential optimization
