# HPO (Hyperparameter Optimization)

This repository extends the foundations of **Linear Regression** toward **Kernelized** and **Regularized** models, integrating **Hyperparameter Optimization (HPO)** for both synthetic (SINC function cretaded using numpy) and real-world data.  
It reproduces the methodology of the _2909Lecture_ notebook — combining **Kernel Ridge Regression (KRR)**, **Bayesian optimization**, and evaluation on both a **toy (sinc)** dataset and the **California Housing** dataset.

---

## Goal and Data

Implements a complete regression pipeline:

- Starts with a **toy nonlinear dataset** defined by the noisy function \( y = \mathrm{sinc}(x) + \epsilon \).
- Applies **Kernel Ridge Regression (RBF kernel)** to capture nonlinear dependencies.
- Tunes the hyperparameters _(regularization α and kernel width γ)_ using **Bayesian Optimization** (`BayesSearchCV`).
- Extends the same approach to the **California Housing** dataset, comparing **Linear**, **Ridge**, and **SGD Regression** models under identical preprocessing and metrics.

Each experiment includes a **train/test split**, evaluation via \( R^2 \), MSE, and residual analysis (true vs predicted values, residual plots, and correlation heatmaps).

---

### Results Summary

---

## Environment

- Python 3.9+
- Libraries:
  - `numpy`
  - `matplotlib`
  - `scikit-learn`
  - `scikit-optimize`
  - `pandas`
  - `seaborn`
  - `statsmodels`
