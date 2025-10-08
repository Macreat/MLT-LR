# Face Embedding Distance Analysis

This notebook implements a practical experiment on **Euclidean geometry in high-dimensional feature spaces**, applied to **face similarity verification**. Using embeddings extracted from facial images, the project evaluates pairwise **Euclidean distances** to determine visual similarity and identity correspondence.

## Objectives

- Demonstrate the use of **Euclidean distance** for facial embedding comparison.
- Analyze distance thresholds to distinguish between **same** and **different** identities.
- Interpret results in the context of **representation bias** and **model ambiguity**.

## Methodology

1. **Image Generation:** Synthetic face samples obtained from _thispersondoesnotexist.com_.
2. **Embedding Extraction:** Deep neural representations generated using **DeepFace**.
3. **Distance Computation:** Pairwise Euclidean distance across all embeddings.
4. **Threshold Decision:** Classification of similarity based on empirical distance thresholds.
5. **Interpretation:** Evaluation of misclassifications and potential bias in embedding space.

## Results

- Lower distances correspond to visually similar identities.
- Some ambiguity observed due to **morphological and representational bias**.
- Demonstrates the geometric foundation behind modern face verification systems.

## Environment

- Python 3.9.13
- Dependencies: `deepface`, `scipy`, `opencv-python`, `numpy`, `matplotlib` / install using pip install -r requirements once the environment is activated.
