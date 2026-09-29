# ACKTransformer – DDoS Attack Detection using Python and Transformers

This project uses **Python** and its powerful machine learning ecosystem to build a **Transformer-based deep learning model** for detecting **ACK fragmentation DDoS attacks**.
The end-to-end workflow — from data preprocessing to model evaluation — is entirely implemented in Python, demonstrating how it can efficiently handle large-scale cybersecurity datasets and deliver high-performance classification results.

---

## Overview

The project implements a **Transformer network (ACKTransformer)** using **PyTorch** for tabular data classification.
It employs **Stratified K-Fold cross-validation** for reliable evaluation and produces detailed visualizations and reports for each fold.

The system automatically:

* Loads and preprocesses network traffic data using **Pandas** and **NumPy**
* Scales features with **StandardScaler**
* Trains and validates the model using **PyTorch**
* Computes classification metrics via **Scikit-learn**
* Generates plots and embeddings using **Matplotlib** and **UMAP**
* Saves trained models, metrics, and visualizations using **Python’s OS utilities**

---

## Python Libraries Used

| Purpose          | Libraries                               |
| ---------------- | --------------------------------------- |
| Data Handling    | `pandas`, `numpy`                       |
| Visualization    | `matplotlib`, `umap-learn`              |
| Machine Learning | `scikit-learn`                          |
| Deep Learning    | `torch`, `torch.nn`, `torch.utils.data` |
| File Management  | `os`, `pathlib`                         |

---

## Project Workflow

1. **Data Preprocessing**
   Load the dataset (`shuffled_merged_data.csv`), replace label values, handle missing data, and scale features using `StandardScaler`.

2. **Model Definition**
   Define the `ACKTransformer` model in PyTorch with input projection, transformer encoder layers, and fully connected output layers.

3. **Training and Validation**
   Perform 5-Fold Stratified Cross-Validation using `StratifiedKFold`.
   Track training/validation loss, accuracy, precision, recall, and F1-score.
   Implement early stopping to prevent overfitting.

4. **Visualization and Reporting**
   Generate and save:

   * Loss and accuracy curves
   * Confusion matrices
   * ROC curves (AUC)
   * UMAP visualizations of feature embeddings
   * Classification reports (CSV)

5. **Model Saving**
   The best model per fold is saved as a `.pth` file for future evaluation or deployment.

---

## Output Structure

```
ddos_results/
│
├── models/        # Saved model checkpoints
├── plots/         # Confusion Matrix, ROC, Loss/Accuracy, UMAP visualizations
└── reports/       # Classification reports for each fold (CSV)
```

---

## Key Highlights

* End-to-end **Python implementation** for cybersecurity attack detection
* **Transformer-based model** adapted for tabular data
* **Cross-validation**, **UMAP visualization**, and **automated reporting**
* Modular design for easy reproducibility and extension

---

## Summary

This project demonstrates how **Python** can serve as a unified environment for **data preprocessing**, **deep learning**, and **performance visualization** in cybersecurity applications.
By combining libraries like PyTorch, scikit-learn, and matplotlib, it provides a complete and reproducible workflow for DDoS attack detection using Transformer-based architectures.

---
