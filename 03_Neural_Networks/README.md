# Neural Networks

Implementation of a simple Artificial Neural Network from scratch using only NumPy.

## Topics Covered

- Limitations of Logistic Regression
- Biological Inspiration
- Artificial Neurons
- Inputs, Weights and Biases
- Activation Functions
- Hidden Layers
- Matrix Representation
- Forward Propagation
- Building a 3 → 2 → 1 Neural Network

## Mathematical Summary

### Weighted Sum

\[
z = Wx + b
\]

### Sigmoid Activation

\[
\sigma(z)=\frac{1}{1+e^{-z}}
\]

### Hidden Layer

\[
Z_1=XW_1+b_1
\]

\[
A_1=\sigma(Z_1)
\]

### Output Layer

\[
Z_2=A_1W_2+b_2
\]

\[
A_2=\sigma(Z_2)
\]

## Files

- `main.ipynb` — Step-by-step implementation and explanation of Forward Propagation.
