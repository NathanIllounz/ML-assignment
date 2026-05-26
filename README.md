# Machine Learning Assignment: Custom KNN MNIST Classifier from Scratch

## 👥 Student Details
* **Name:** Nathan I.
* **ID:** 328587423
* **Course:** Machine Learning Assignment – Image Processing (עיבוד תמונה)

---

## 📋 Project Overview
This project implements a **K-Nearest Neighbors (KNN)** image classification model from scratch using optimized NumPy vectorization to recognize handwritten digits from the MNIST dataset. 

Following the formal definition of Machine Learning:
* **Task (T):** Correct classification of handwritten digits (0–9).
* **Performance Measure (P):** Macro-average F1-score to treat all digit classes equally and prevent class frequency bias.
* **Experience (E):** Ingesting and storing the 60,000 raw MNIST training samples.

### 🔧 Feature Engineering Pipeline
1. **IDX Unpacking:** Custom binary parsing of low-level `.idx3-ubyte` and `.idx1-ubyte` file streams into structured matrices.
2. **Vectorization:** Flattening 2D spatial pixel images ($28 \times 28$) into a single 1D feature array of 784 coordinates.
3. **MinMax Normalization:** Scaling raw pixel intensities from a `0–255` range down to a continuous `0.0–1.0` range to prevent geometric distance distortions.

---

## 📊 Hyperparameter Tuning & Cross-Validation Results
We built a custom **5-Fold Cross-Validation Grid Search** from scratch to evaluate parameter configurations across a dynamic training partition pool.

| K Value | Distance Metric | Mean Macro-F1 Score |
| :---: | :---: | :---: |
| 1 | Euclidean ($L_2$ Norm) | **0.8596 (Optimal)** |
| 3 | Euclidean ($L_2$ Norm) | 0.8332 |
| 5 | Euclidean ($L_2$ Norm) | 0.8165 |
| 7 | Euclidean ($L_2$ Norm) | 0.8149 |
| 1 | Manhattan ($L_1$ Norm) | 0.8319 |
| 3 | Manhattan ($L_1$ Norm) | 0.8137 |
| 5 | Manhattan ($L_1$ Norm) | 0.8079 |
| 7 | Manhattan ($L_1$ Norm) | 0.7838 |

**Optimal System Configuration:** $K=1$, Distance Metric: **Euclidean**.  
*Retrained final model test evaluation slice score:* **0.9902**

---

## 🔗 Submission Artifacts
* **Jupyter Notebook:** [src_notebook.ipynb](src_notebook.ipynb) (Rendered with all dataframes, shape verifications, and visualizations)
* **Technical Walkthrough Video (YouTube):** [PASTE YOUR YOUTUBE VIDEO LINK HERE]
* **Kaggle Dataset Source:** [MNIST Handwritten Digits](https://www.kaggle.com/datasets/hojjatk/mnist-dataset)
