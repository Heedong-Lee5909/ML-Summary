# Regularization in Linear Regression

## Overview
Regularization is a regression technique to prevent overfitting. It constrains the model during training, discouraging it from overfitting to the training data. Regularization achieves this goal by suppressing the size of its coefficients.

A **regularized cost function** has the general form:

regularized cost = mean squared error + lambda * penalty term

- **lambda**: Parameter controlling the influence of the penalty term
- **penalty term**: Measures the size of the coefficients

Common methods:
- **Ridge Regression**: L2 penalty (sum of squares of coefficients)
- **Lasso Regression**: L1 penalty (sum of absolute values of coefficients)

## Linear Regression
In ordinary linear regression, predictions are a linear combination of features:

y_hat = theta_0 + theta_1 * x_1 + theta_2 * x_2 + ... + theta_n * x_n

- `x_i`: Feature values
- `theta_0`: Intercept term
- `theta_i`: Coefficients (weights)

Goal: Minimize the mean squared error (MSE) between predicted and actual values.

## Ridge vs Lasso vs Linear Regression
- **Linear Regression**: No penalty term.
- **Ridge Regression**: Adds L2 penalty → shrinks coefficients but does not set them to zero.
- **Lasso Regression**: Adds L1 penalty → can shrink some coefficients to exactly zero (feature selection).

## Sparse Coefficients Scenario
- High Signal-to-Noise Ratio (SNR): All three methods predict non-zero coefficients well. Lasso finds zero coefficients exactly.
- Low SNR: Linear regression overestimates and mispredicts zero coefficients. Ridge and lasso perform better, with lasso superior for identifying zero coefficients.

## Non-Sparse Coefficients Scenario
- High SNR: All methods predict well. Lasso identifies zero coefficients accurately.
- Low SNR: Linear regression performs poorly; ridge slightly outperforms lasso for non-zero coefficients, but lasso is better for finding zero coefficients.

## Performance Summary
- Lasso consistently outperforms ridge and linear regression in sparse and noisy environments.
- Ridge is stable across scenarios but less effective for feature selection.
- Linear regression is most sensitive to noise.

## Example Results
Test performance on moderately noisy data:
- Lasso predictions closely align with actual values.
- Lasso's MSE is ~30 times smaller than ridge and linear regression.

## Key Takeaways
- Regularization mitigates overfitting in linear regression.
- Ridge regression uses L2 penalty; lasso regression uses L1 penalty.
- Lasso is especially useful for feature selection in sparse datasets.
- Choice of method depends on data noise level and sparsity.
