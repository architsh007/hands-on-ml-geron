# Chapter 5 — Support Vector Machines (SVM)

This chapter explores Support Vector Machines from a geometric and optimization perspective.
The goal is to understand not only how to use SVMs, but why they generalize well and how
their hyperparameters control model complexity.

---

## 📌 Learning Objectives

- Understand margin maximization
- Differentiate hard-margin and soft-margin SVM
- Interpret the role of C (regularization)
- Understand support vectors and constraint optimization
- Apply the kernel trick for nonlinear classification
- Analyze RBF and polynomial kernels
- Implement Support Vector Regression (SVR)
- Understand SVM scalability limitations

---

## 📓 Notebooks Overview

### 1️⃣ Linear SVM: Hard vs Soft Margin
- Maximum margin classifier
- Slack variables
- Effect of C on bias–variance tradeoff
- Visualization of decision boundaries

### 2️⃣ Kernel Trick & Nonlinear SVM
- Why linear SVM fails on nonlinear data
- Polynomial kernel
- RBF kernel
- Hyperparameter interaction (C & gamma)
- Visual analysis of overfitting and underfitting

### 3️⃣ Support Vector Regression (SVR)
- ε-insensitive loss
- Comparison with MSE
- Interpretation of support vectors in regression

### 4️⃣ SVM vs Logistic Regression
- Compares two margin-based linear classifiers from theoretical and practical perspectives.
- Logistic loss vs hinge loss
- Margin maximization vs probabilistic modeling
- Robustness to noise
- Scalability comparison
- When to prefer SVM vs Logistic Regression

---

## 🧠 Key Insights

- Only support vectors determine the decision boundary
- C controls the tradeoff between margin width and constraint violations
- Gamma controls locality of influence in the RBF kernel
- Kernel trick enables implicit high-dimensional feature mappings
- SVM complexity depends on the number of support vectors
- Logistic regression produces calibrated probabilities, SVM does not
- Kernel SVMs scale poorly for very large datasets
- Linear SVM is highly effective in high-dimensional sparse spaces (e.g., text)

---

## ⚙️ Engineering Tradeoffs

| Aspect                 | Logistic Regression        | SVM                       |
| ---------------------- | -------------------------- | ------------------------- |
| Loss Function          | Logistic loss              | Hinge loss                |
| Output                 | Probabilities              | Margins                   |
| Robustness to Outliers | Moderate                   | High (margin-based)       |
| Scalability            | Excellent                  | Moderate to Poor (kernel) |
| Nonlinear Extension    | Manual feature engineering | Kernel trick              |

---

## 🛠 Tools Used

- Python
- NumPy
- Matplotlib
- Scikit-learn