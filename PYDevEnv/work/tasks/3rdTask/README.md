# Linear Regression and SGD Regression Analysis

This repository contains two complementary notebooks demonstrating the foundations of **Linear Regression** — both in its **analytical (closed-form)** and **iterative (gradient-based)** forms.  
The work uses standard datasets ( a ToySet and _California Housing_) to explore regression performance, diagnostics, and optimization dynamics.

---

## Goal and data

Implements a **baseline linear regression** on a tabular dataset ( first on a 'toySet' and continuing with the `fetch_california_housing`).  
Performs a standard **train/test split**, evaluates the model with $$R^2$$, MSE, and MAPE,  
 and visualizes **residuals** (including a **QQ plot**, **L2 regularization**, **learning rate decay and early stopping**.) to assess each model validity.

---

### Results Summary

#### Linear Regression vs SGD Regression

• Both methods achieve nearly identical parameter estimates and prediction performance when applied to the same dataset, validating that Stochastic Gradient Descent (SGD) converges toward the closed-form Ordinary Least Squares (OLS) solution.

• The closed-form (analytical) Linear Regression computes the optimal coefficients in one step, providing exact results but at higher computational cost for large or high-dimensional datasets.

• The SGD implementation, although iterative, allows efficient training on large-scale data by updating parameters in mini-batches and incorporating regularization (L2 penalty).

• Performance metrics (MSE, MAE, R²) remain equivalent across both methods, confirming numerical consistency and correctness of the gradient-based optimization.

• Visualization of residuals and predicted vs real values shows overlapping patterns, proving that both learning paradigms capture the same linear relationships in the data.

• Overall, **Linear Regression** offers precision and simplicity for small datasets, while **SGD Regression** provides scalability, control over learning dynamics, and better adaptability for streaming or big data scenarios.

## Environment

- Python 3.9+
- Libraries: `numpy`, `matplotlib`, `scikit-learn`, `statsmodels`
