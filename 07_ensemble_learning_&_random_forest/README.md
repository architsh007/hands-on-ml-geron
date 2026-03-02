# Chapter 7 — Ensemble Learning & Random Forests

This chapter explores ensemble methods from a bias–variance and statistical learning perspective.  
The objective is to understand *why* ensembles work, not just how to implement them.

We analyze:

- Voting classifiers (hard vs soft)
- Bagging and variance reduction
- Random Forest and feature randomness
- Stacking and meta-learning
- Bias–variance tradeoffs in ensembles

---

## Learning Objectives

By the end of this chapter, you should be able to:

- Explain why averaging reduces variance
- Derive the ensemble variance formula
- Understand correlation between base learners
- Differentiate bagging and boosting conceptually
- Interpret soft vs hard voting mathematically
- Implement stacking without data leakage
- Analyze when ensembles fail to improve performance

---

## Core Theoretical Insight

For an ensemble of correlated models:

\[
Var(\hat{f}_{ensemble}) = \rho \sigma^2 + \frac{1 - \rho}{T} \sigma^2
\]

Where:

- \( \sigma^2 \) = variance of individual model  
- \( \rho \) = correlation between models  
- \( T \) = number of estimators  

Key takeaway:

- Increasing **T** reduces variance
- Reducing **correlation (ρ)** is critical
- If models are highly correlated, ensembles provide little gain

---

## Notebook Overview

### 1️⃣ Voting Classifiers (`01_voting_classifiers.ipynb`)

- Hard Voting (majority rule)
- Soft Voting (probability averaging)
- Bias–variance interpretation
- Decision boundary visualization
- When soft voting outperforms hard voting

Key insight:
> Soft voting preserves probability information and typically produces smoother, more stable decision boundaries.

---

### 2️⃣ Bagging vs Single Tree (`02_bagging_vs_single_tree.ipynb`)

- Deep decision tree overfitting
- Bootstrap sampling
- Variance reduction through averaging
- Out-of-bag (OOB) evaluation
- Decision boundary smoothing

Key insight:
> Bagging reduces variance without increasing bias and rarely overfits as the number of estimators increases.

---

### 3️⃣ Stacking Classifier (`03_stacking_classifier.ipynb`)

- Heterogeneous base learners
- Out-of-fold predictions to prevent leakage
- Logistic regression as meta-model
- Comparison with voting
- Bias–variance analysis

Stacking formulation:

\[
z = [f_1(x), f_2(x), ..., f_k(x)]
\]

\[
\hat{y} = g(z)
\]

Key insight:
> Stacking learns optimal combination weights and is most effective when base model errors are uncorrelated.

---

## Ensemble Method Comparison

| Method        | Structure      | Reduces Bias | Reduces Variance | Overfitting Risk |
|--------------|---------------|--------------|------------------|------------------|
| Hard Voting  | Parallel       | No           | Yes              | Low              |
| Soft Voting  | Parallel       | Slight       | Yes              | Low              |
| Bagging      | Parallel       | No           | Strongly         | Very Low         |
| Random Forest| Parallel + Feature Randomness | No | Strongly | Very Low |
| Stacking     | Two-layer      | Possible     | Possible         | Moderate         |

---

## Practical Engineering Insights

- Diversity is as important as accuracy in ensembles.
- Soft voting is a strong baseline before stacking.
- Bagging primarily reduces variance.
- Boosting (covered separately) reduces bias sequentially.
- Increasing number of trees in bagging:
  - Does not increase overfitting
  - Reduces variance asymptotically
- Complex meta-models in stacking increase variance risk.

---

## Experimental Observations

On the synthetic moons dataset:

- SVC alone performed strongly.
- Soft voting slightly improved stability.
- Stacking provided marginal gain.
- When one model dominates performance, stacking yields diminishing returns.

Ensemble performance depends on:

Accuracy + Diversity

---

## Tools Used

- Python
- NumPy
- Matplotlib
- Scikit-learn

---

## Chapter Takeaways

- Ensemble methods primarily improve **stability**.
- Variance reduction is achieved through averaging decorrelated models.
- Stacking requires careful handling of data leakage.
- Strong base learners limit ensemble gains.
- Correlation between models determines ensemble effectiveness.
