# Chapter 4 — Training Models

This chapter focuses on the mathematical and algorithmic foundations of
how machine learning models are trained, optimized, and evaluated.

The goal is not only to apply models using libraries, but to understand
*why* they work, *how* they fail, and *how* to diagnose and fix those failures.

The notebooks in this chapter follow the structure of
*Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow*
by Aurélien Géron, with additional explanations, visualizations,
and from-scratch implementations.

---

## 📌 Learning Objectives

By completing this chapter, I aimed to:

- Understand linear models at a mathematical level
- Implement gradient descent from scratch
- Diagnose bias vs variance using learning curves
- Understand model capacity and overfitting
- Apply regularization to control complexity
- Extend regression models to classification via logistic regression

---

## 📓 Notebooks Overview

### 1️⃣ Linear Regression from Scratch  
**`01_linear_regression_from_scratch.ipynb`**

This notebook implements linear regression without relying on high-level
machine learning libraries.

Key topics:
- Linear regression hypothesis function
- Mean Squared Error (MSE) loss
- Gradient descent optimization
- Learning rate effects
- Loss surface visualization
- Batch vs iterative optimization

**Key takeaway:**  
Optimization is not a black box — it is a geometric and mathematical process.

---

### 2️⃣ Learning Curves & Bias–Variance Diagnosis  
**`02_learning_curves.ipynb`**

This notebook demonstrates how learning curves can be used to diagnose
underfitting and overfitting in practice.

Key topics:
- Training vs validation error
- High bias vs high variance patterns
- Effect of dataset size
- Polynomial regression and model capacity
- Visual diagnosis of generalization behavior

**Key takeaway:**  
Poor performance is not a single problem — learning curves reveal *why* a model fails.

---

### 3️⃣ Logistic Regression  
**`03_logistic_regression.ipynb`**

This notebook introduces logistic regression as a probabilistic
classification model.

Key topics:
- Sigmoid function and probability estimation
- Decision boundaries
- Cross-entropy (log loss)
- Relationship to linear regression
- Visualization of classification confidence

**Key takeaway:**  
Logistic regression is a linear model with a probabilistic interpretation,
not just a classification heuristic.

---

## 🧠 Key Concepts Demonstrated

- Optimization vs closed-form solutions
- Gradient descent and convergence
- Bias–variance tradeoff
- Model capacity and regularization
- Probability-based classification

---

## 🛠 Tools & Libraries Used

- Python
- NumPy
- Matplotlib
- Scikit-learn

---

## 🎯 Why This Chapter Matters

Understanding how models are trained is essential for:
- debugging model failures
- choosing appropriate model complexity
- interpreting performance metrics
- building reliable and generalizable systems

This chapter builds the foundation for more advanced models such as
Support Vector Machines, Decision Trees, and Neural Networks.
