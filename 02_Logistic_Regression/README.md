# Logistic Regression

Implementation of **Binary Logistic Regression** from scratch using only NumPy.

## Topics Covered

- Why Linear Regression fails for Classification
- Binary Classification
- Sigmoid Function
- Decision Boundary
- Binary Cross-Entropy Loss
- Gradient Computation
- Gradient Descent
- Model Training
- Predictions

## Mathematical Summary

### Linear Model

\[
z=wx+b
\]

### Sigmoid Function

\[
\sigma(z)=\frac1{1+e^{-z}}
\]

### Binary Cross-Entropy Loss

\[
L
=
-\left(
y\log(p)
+
(1-y)\log(1-p)
\right)
\]

### Gradients

Weight

\[
\frac{\partial L}{\partial w}
=
\frac1n\sum(p-y)x
\]

Bias

\[
\frac{\partial L}{\partial b}
=
\frac1n\sum(p-y)
\]

### Gradient Descent

\[
w=w-\alpha\frac{\partial L}{\partial w}
\]

\[
b=b-\alpha\frac{\partial L}{\partial b}
\]

## Files

- `main.ipynb` — Step-by-step implementation and explanations.
