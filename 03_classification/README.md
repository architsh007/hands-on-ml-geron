# Chapter 3 — Classification

This chapter explores classification problems and evaluation strategies using
the MNIST dataset as a running example. The focus is not only on building models,
but on understanding *how and why* classification systems fail.

Rather than optimizing for accuracy, this chapter emphasizes error analysis,
decision thresholds, and metric selection under class imbalance.

---

## Topics Covered

### 1. Binary Classification & Class Imbalance
- Framing MNIST as a 5 vs not-5 problem
- Demonstrating why accuracy is misleading
- Using confusion matrices to expose failure modes

### 2. Precision, Recall & Decision Thresholds
- Formal definitions and intuition
- Trade-off between false positives and false negatives
- Manual threshold adjustment using decision scores
- Precision–Recall curves

### 3. ROC Curves & AUC
- True Positive Rate vs False Positive Rate
- Threshold-free evaluation
- Probabilistic interpretation of AUC
- Why ROC can be misleading for rare-event detection

### 4. Multiclass Classification
- One-vs-Rest strategy for multiclass problems
- Multiclass confusion matrix analysis
- Error-focused visualization to identify systematic confusions

### 5. Multiclass Evaluation Metrics
- Per-class precision, recall, and F1
- Macro, micro, and weighted averaging
- When each averaging method is appropriate
- Why accuracy and micro-averaged metrics can hide critical failures

---

## Key Takeaways

- Accuracy alone is insufficient for evaluating classification models.
- Confusion matrices reveal *where* and *why* models fail.
- Precision and recall must be traded off based on application-specific costs.
- ROC and PR curves answer different questions and must be chosen carefully.
- Macro vs micro averaging reflects different values and priorities.
- Error analysis should guide feature engineering and model improvement.

---

## Notebooks

| Notebook | Description |
|--------|-------------|
| `01_accuracy_vs_confusion_matrix.ipynb` | Demonstrates why accuracy fails under class imbalance |
| `02_precision_recall_thresholds.ipynb` | Explores threshold-based trade-offs |
| `03_roc_vs_pr_curves.ipynb` | Compares ROC and PR curves |
| `04_multiclass_error_analysis.ipynb` | Multiclass confusion matrix analysis |

---

## Why This Matters

Classification systems are decision-making systems.  
Understanding metrics, error trade-offs, and evaluation biases is essential for
building models that work in real-world, high-stakes applications.
