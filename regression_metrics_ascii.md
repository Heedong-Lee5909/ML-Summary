
# Regression Metrics and Evaluation Techniques

This summary outlines key points from the video on Regression Metrics and Evaluation Techniques.

## Purpose

Evaluating a regression model involves determining how accurately it can predict continuous numerical values (e.g., exam grades). The difference between predicted and actual values is called the **error**.

## Common Regression Metrics

### 1. Mean Absolute Error (MAE)
The average absolute difference between predicted values and actual values.

```
MAE = (1/n) * Σ |yᵢ - ŷᵢ|
```

### 2. Mean Squared Error (MSE)
The average of the squared differences between predicted and actual values.

```
MSE = (1/n) * Σ (yᵢ - ŷᵢ)²
```

### 3. Root Mean Squared Error (RMSE)
The square root of MSE. Same unit as the target variable.

```
RMSE = sqrt( (1/n) * Σ (yᵢ - ŷᵢ)² )
```

### 4. R-squared (R²)
Represents the proportion of variance in the target variable that is explained by the model.

```
R² = 1 - (SS_res / SS_tot)
```

- **R² = 1** → Perfect model  
- **R² = 0** → Model explains nothing  
- **R² < 0** → Model performs worse than a constant mean predictor

## Explained Variance

Explained variance is the sum of squared differences between predictions and the average target value. A good model has high explained variance.

## Visualization

You should **visualize predicted vs. actual values** to complement metric analysis. Regression models can be evaluated on how close the predictions fall to the actual data points, ideally lying close to the best-fit line.

## Notes on R²

- Intuitive for non-technical stakeholders ("explains 85% of outcome variability")
- Only appropriate when the relationship is linear
- Can be misleading for nonlinear models

## Model Comparison Example

Three linear models were trained on a log-normal target distribution:
1. Original target
2. Box-Cox transformed target
3. Log transformed target

Metrics such as MAE, MSE, RMSE, and R² improved after transformations, aligning with visual improvement of model fit.

## Summary

- **MAE**: Average of absolute errors
- **MSE**: Average of squared errors
- **RMSE**: Root of MSE
- **R²**: Variance explained by the model

Visual tools and multiple metrics together provide a more reliable picture of model performance.
