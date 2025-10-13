# 2D Vector Projection Analysis

This notebook explores the mathematical and computational process of **vector projection** using both analytical and iterative (gradient descent) methods.  
Through three progressive subtasks, the experiment extends from basic 2D vector projection to image-space projection using least-squares minimization.

---

## Objectives

- Demonstrate the equivalence between **analytical** and **gradient descent** approaches in vector projection.
- Apply least-squares optimization to approximate the projection coefficient **c\*** iteratively.
- Extend projection concepts from 2D vectors to **high-dimensional image vectors**.
- Visualize and compare analytical vs numerical convergence and projection results.

---

## Methodology

1. **Subtask 1 – 2D Vector Projection (Analytical vs GD):**  
   Analytical derivation of the projection formula  
   and iterative reconstruction via gradient descent minimization.

2. **Subtask 2 – Least Squares and Cost Convergence:**  
   Implementation of the cost function  
    J(c) = \|a - c b\|^2
   and tracking of both the convergence of _c_ and decay of _J(c)_.

3. **Subtask 3 – Image Vector Projection:**  
   Loading grayscale facial images, flattening them into vectors, and computing projections between modified and reference images using both analytical and GD solutions.  
   Reconstruction of the projected vectors back into images for visual comparison.

---

## Results

- Analytical and gradient descent methods yield **identical projection results** within numerical precision.
- Gradient descent coefficient **converges** rapidly to the analytical value **c\***.
- Projection coefficient interpretation:
  - c\* ≈ 1 → images or vectors are nearly identical.
  - c\* > 1 → projected vector (or image) is **brighter / stronger**.
  - c\* < 1 → projected vector (or image) is **weaker / less correlated**.
  - c\* ≈ 0 → vectors are **independent or unrelated**.
- The image projection experiment visually confirms correlation between **intensity and geometric similarity**.

---

## Environment

- **Python:** 3.9+
- **Dependencies:**  
  `numpy`, `matplotlib`, `opencv-python`, `scipy`
- Optional: `notebook` or `jupyterlab` for interactive visualization.

Install dependencies:

```bash
pip install -r requirements.txt
```
