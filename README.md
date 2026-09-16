# Breast Cancer Prediction with Logistic Regression

Classifying breast tumors as malignant or benign using logistic regression, built on the Wisconsin Diagnostic Breast Cancer dataset.

## Dataset

[Breast Cancer Wisconsin (Diagnostic) Data Set](https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data) — 569 samples, 30 numeric features computed from digitized images of breast mass cell nuclei (radius, texture, perimeter, smoothness, etc.), target: `diagnosis` (Malignant / Benign).

## What this project covers

- **Data cleaning** — dropped irrelevant `id` column and empty `Unnamed: 32` column, encoded `diagnosis` (M/B) to binary (1/0)
- **Preprocessing** — feature scaling with `StandardScaler`, train/test split (70/30)
- **Modeling** — logistic regression (`scikit-learn`)
- **Evaluation** — accuracy, classification report (precision, recall, F1-score per class)

## Results

The model achieved **98.25% accuracy** on the test set. Unlike a typical imbalanced classification problem, this dataset's two classes are well-represented, and the model performs strongly and consistently across both:

| Class | Precision | Recall | F1-score |
|---|---|---|---|
| Benign (0) | 0.99 | 0.98 | 0.99 |
| Malignant (1) | 0.97 | 0.98 | 0.98 |

High precision and recall on **both** classes — not just the majority one — confirms the model is genuinely learning to distinguish malignant from benign cases, rather than exploiting class imbalance.

## Tools

Python, pandas, scikit-learn, seaborn, matplotlib

## Note

Built for learning purposes — not intended for real medical diagnosis.
