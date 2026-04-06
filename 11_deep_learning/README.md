🧠 Chapter 11 — Deep Learning with Keras (TensorFlow)

---

📌 Overview

This chapter introduces practical deep learning using the Keras API in TensorFlow.
We transition from theoretical neural networks to building trainable models with automatic differentiation.

Deep learning models can be represented as:

$$
a = \phi(Wx + b)
$$

where:

- $W$ = weights
- $b$ = bias
- $\phi$ = activation function

---

🎯 Objectives

- Build neural networks using the Keras Sequential API
- Understand the training pipeline
- Visualize learning dynamics
- Improve model performance using modern techniques

---

📂 Notebooks

1️⃣ Keras Sequential Basics

- Model creation using "Sequential"
- Training with "model.fit()"
- Evaluation on test data

Core pipeline:

$$
\text{Input} \rightarrow \text{Forward Pass} \rightarrow \text{Loss} \rightarrow \text{Backpropagation} \rightarrow \text{Update}
$$

---

2️⃣ Decision Boundary Visualization

- Compare shallow vs deep networks
- Visualize learned decision boundaries

Key idea:

$$
f(x) = f_3(f_2(f_1(x)))
$$

Deep networks learn compositional functions.

---

3️⃣ Training Improvements

- Batch Normalization
- Dropout Regularization

Loss with regularization:

$$
L = L_{\text{data}} + \lambda ||W||^2
$$

---

⚙️ Training Pipeline

🔹 Model Compilation

model.compile(optimizer="adam", loss="binary_crossentropy")

Defines:

- Optimizer: $w \leftarrow w - \eta \nabla L$
- Loss: error function
- Metrics: evaluation criteria

---

🔹 Model Training

model.fit(X, y)

Performs:

$$
\text{Forward Pass} \rightarrow \text{Loss Computation} \rightarrow \text{Gradient Computation} \rightarrow \text{Weight Update}
$$

---

🔬 Core Concepts

🔹 Activation Functions

- ReLU:

$$
\text{ReLU}(x) = \max(0, x)
$$

- Sigmoid:

$$
\sigma(x) = \frac{1}{1 + e^{-x}}
$$

---

🔹 Optimization

- SGD:

$$
w = w - \eta \nabla L
$$

- Adam (adaptive optimization)

---

🔹 Loss Function (Binary Classification)

$$
L = -\left[y \log(\hat{y}) + (1-y)\log(1-\hat{y})\right]
$$

---

⚠️ Training Challenges

- Vanishing gradients
- Exploding gradients
- Overfitting

---

✅ Solutions

- ReLU activation
- Batch Normalization
- Dropout
- Adam optimizer

---

🧠 Key Insights

- Neural networks learn nonlinear decision boundaries
- Depth enables hierarchical feature learning
- Training stability is critical
- Keras abstracts complex training logic

---

🔁 Conceptual Flow

$$
\text{Linear Models} \rightarrow \text{Neural Networks} \rightarrow \text{Deep Learning Systems}
$$

---
