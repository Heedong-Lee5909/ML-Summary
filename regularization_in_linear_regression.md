# Regularization in Linear Regression

## 1. Definition
Regularization is a regression technique used to prevent overfitting. It constrains the model during training, discouraging it from fitting too closely to the training data by suppressing the size of its coefficients.

A modified cost function is used:

    Regularized Cost Function:  J(θ) = MSE + λ · Penalty Term

- λ (lambda): Hyperparameter controlling the influence of the penalty term.
- Penalty: A measurement of coefficient size (e.g., L1, L2 norms).

## 2. Linear Regression
Linear regression models the relationship between two or more variables by fitting a straight line to the dataset.

Prediction equation:

    ŷ = θ₀ + θ₁x₁ + θ₂x₂ + ... + θₙxₙ

- Goal: Minimize Mean Squared Error (MSE).
- No penalty term → Sensitive to noise, prone to overfitting.

## 3. Ridge Regression (L2 Regularization)
Ridge regression adds an L2 penalty term (sum of squared coefficients) to the cost function:

    Cost Function:  J(θ) = MSE + λ * Σ(θⱼ²)

- Helps shrink coefficients.
- Reduces model variance but may not set coefficients to zero.

## 4. Lasso Regression (L1 Regularization)
Lasso regression adds an L1 penalty term (sum of absolute values of coefficients) to the cost function:

    Cost Function:  J(θ) = MSE + λ * Σ|θⱼ|

- Can shrink some coefficients to exactly zero → Useful for feature selection.
- Works well with sparse data.

## 5. Performance Comparison

### Sparse Coefficients (High SNR)
- All three methods predict non-zero coefficients well.
- Lasso finds zero coefficients exactly.
- Ridge and Linear struggle slightly more with zero coefficients.

### Sparse Coefficients (Low SNR)
- Linear regression performs poorly: overestimates coefficients, assigns incorrect large values.
- Ridge and Lasso perform similarly on non-zero coefficients.
- Lasso much better at identifying zero coefficients.

### Non-Sparse Coefficients (High SNR)
- All three predict well; Ridge slightly less accurate than Linear and Lasso.
- Lasso still finds zero coefficients when present.

### Non-Sparse Coefficients (Low SNR)
- Linear regression performs poorly: overestimates coefficients, sensitive to noise.
- Ridge slightly better at non-zero coefficients than Lasso.
- Lasso better at identifying zero coefficients.

## 6. Key Takeaways
- Regularization reduces overfitting risk.
- Ridge (L2) → Shrinks coefficients but keeps all features.
- Lasso (L1) → Shrinks some coefficients to zero → Good for feature selection.
- In noisy environments, regularization significantly outperforms ordinary linear regression.
