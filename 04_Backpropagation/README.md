# Backpropagation

Implementation of Backpropagation from scratch using only NumPy.

## Topics Covered

- Why Neural Networks Need Backpropagation
- Forward Propagation Review
- Binary Cross-Entropy Loss
- Gradients
- The Chain Rule
- Output Layer Gradients
- Hidden Layer Gradients
- Gradient Descent
- Parameter Updates
- Training Loop

## Mathematical Summary

### Forward Propagation

$$
Z_1 = XW_1 + b_1
$$

$$
A_1 = \sigma(Z_1)
$$

$$
Z_2 = A_1W_2 + b_2
$$

$$
A_2 = \sigma(Z_2)
$$

### Binary Cross-Entropy Loss

$$
L =
-\left(
y\log(A_2)
+
(1-y)\log(1-A_2)
\right)
$$

### Output Layer Error

$$
dZ_2 = A_2 - y
$$

### Output Layer Gradients

$$
dW_2 = A_1^T dZ_2
$$

$$
db_2 = \sum dZ_2
$$

### Hidden Layer Error

$$
dZ_1 =
(dZ_2W_2^T)
\odot
\sigma'(Z_1)
$$

### Hidden Layer Gradients

$$
dW_1 = X^T dZ_1
$$

$$
db_1 = \sum dZ_1
$$

### Gradient Descent

$$
W = W - \alpha dW
$$

$$
b = b - \alpha db
$$

## Files

- `main.ipynb` — Step-by-step implementation of Backpropagation and Gradient Descent using NumPy.
