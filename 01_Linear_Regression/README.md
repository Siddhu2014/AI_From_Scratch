# Linear Regression

Implementation of **Simple Linear Regression** from scratch using only NumPy.

## Topics Covered

- Introduction to Linear Regression
- Linear Equation
- Predictions
- Mean Squared Error (MSE)
- Cost Function
- Gradient Descent
- Weight & Bias Updates
- Model Training
- Predictions on New Data

## Mathematical Summary

### Linear Model

\[
\hat{y}=wx+b
\]

### Mean Squared Error

\[
MSE=\frac1n\sum(\hat y-y)^2
\]

### Gradients

Weight

\[
\frac{\partial L}{\partial w}
=
\frac2n\sum(\hat y-y)x
\]

Bias

\[
\frac{\partial L}{\partial b}
=
\frac2n\sum(\hat y-y)
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
