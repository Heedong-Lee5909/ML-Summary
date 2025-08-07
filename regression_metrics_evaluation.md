# 📉 Regression Metrics and Evaluation Techniques

This document summarizes key techniques and metrics for evaluating regression models.

---

## 🎯 Learning Objectives

After studying this topic, you will be able to:

- Explain why evaluating regression models is essential  
- Define regression model errors  
- Describe and compare common regression metrics: MAE, MSE, RMSE, and R²  

---

## ⚠️ Why Evaluate Regression Models?

Regression models predict **continuous values** (e.g., exam scores), but are prone to **prediction errors**. Evaluation is needed to:

- Measure accuracy
- Understand error distribution and magnitude
- Assess model suitability for real-world applications

---

## ❗ What Is Model Error?

- In linear regression, **errors** are the differences between the actual data points and the predicted values (regression line).
- Each point has a residual:  
  \[
  \text{Error}_i = \hat{y}_i - y_i
  \]

---

## 📐 Common Regression Metrics

### 1. **MAE** – Mean Absolute Error  
Average absolute differences between predicted and actual values.  
\[
\text{MAE} = \frac{1}{n} \sum_{i=1}^{n} |\hat{y}_i - y_i|
\]  
**Interpretation:** Easy to understand; treats all errors equally.

---

### 2. **MSE** – Mean Squared Error  
Average of squared differences between predicted and actual values.  
\[
\text{MSE} = \frac{1}{n - p} \sum_{i=1}^{n} (\hat{y}_i - y_i)^2
\]  
Where \( p \) is the number of parameters in the model.  
**Interpretation:** Penalizes larger errors more than MAE.

---

### 3. **RMSE** – Root Mean Squared Error  
Square root of the MSE.  
\[
\text{RMSE} = \sqrt{\text{MSE}}
\]  
**Interpretation:** Has the same unit as the target variable → easier to interpret than MSE.

---

### 4. **R² Score** – Coefficient of Determination  
Measures the proportion of variance in the dependent variable explained by the independent variables.  
\[
R^2 = 1 - \frac{\text{Unexplained Variance}}{\text{Total Variance}}
\]  
- **Range:** 0 to 1 (can be negative)
  - **1** → perfect prediction  
  - **0** → predicts only the mean  
  - **< 0** → worse than mean model

---

## 📊 Explained Variance

- Sum of squared differences between predicted values and the **mean** of the actual target variable.
- R² is derived from explained and unexplained variance.

---

## 🧪 Visual Evaluation

- Always **plot predicted vs. actual values**  
- Use **residual plots** to detect patterns and heteroscedasticity
- Use **transformations** (e.g., log, Box-Cox) if the target variable is not normally distributed

---

## 🧠 Example: Improving Model Fit

- Three regression models are compared using:
  - Raw target values
  - Log-transformed target
  - Box-Cox-transformed target
- After transformation:
  - **R² increases**
  - **MAE, MSE, RMSE decrease**
  - The data aligns more closely with the regression line

---

## ✅ Summary

- **Regression evaluation** ensures model reliability for continuous predictions.
- **MAE, MSE, RMSE** quantify prediction error in different ways.
- **R²** shows how much variation the model explains.
- Always visualize results and consider transformations for non-normal targets.