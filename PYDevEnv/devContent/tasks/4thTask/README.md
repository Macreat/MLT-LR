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

- Hyperparameter Optimization (HPO) via Bayesian Search effectively tuned α (regularization) and γ (kernel width) for the RBF Kernel Ridge model, yielding balanced bias–variance tradeoffs in both synthetic and real datasets.
- On the sinc dataset, the RBF kernel achieved a smooth nonlinear fit that captured the underlying trend while filtering out noise, confirming the effectiveness of kernel-based regression for nonlinearly separable data.
- In the California Housing dataset, the RBF Kernel Ridge produced slightly better generalization than the polynomial and linear models, maintaining stable MSE and R2
  across train/test splits.
- The Polynomial Regression baseline showed higher variance and overfitting tendencies, especially under noisy or complex feature relationships.
- this notebook demonstrates that kernel-based models, when coupled with principled HPO, outperform fixed or manually tuned baselines — achieving smoother predictions, better generalization, and consistent performance across both synthetic and real-world regression problems.

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
