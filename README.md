# 💳 Credit Card Fraud Detection

This project explores both **unsupervised anomaly detection** and **supervised classification** methods to identify fraudulent credit card transactions in a highly imbalanced dataset (~0.17% fraud rate).

---

## Methods Used

**Day 1: EDA + Preprocessing**
- Scaled `Amount` and `Time` features
- Visualized class imbalance & correlations
- Train/test split created

**Day 2: Anomaly Detection (Unsupervised)**
- Univariate Gaussian
- Multivariate Gaussian
- Selected best threshold (ε) using F1 score on validation set

**Day 3: Supervised Learning**
- Applied PCA for dimensionality reduction
- Trained Logistic Regression on reduced data
- Evaluated performance

**Day 4: Hybrid Model + Evaluation**
- Combined predictions from all models
- Compared Precision, Recall, F1, Confusion Matrix
- Focused on **recall-heavy strategy** (fraud detection prioritizes recall)

---

## Final Model Performance

| Model                 | Precision | Recall | F1     |
|----------------------|-----------|--------|--------|
| Univariate Gaussian   | 0.0646    | 0.8878 | 0.1204 |
| Multivariate Gaussian | 0.0147    | 0.8980 | 0.0289 |
| Logistic Regression   | 0.0024    | 0.6939 | 0.0047 |
| Hybrid Model          | 0.0030    | 0.9694 | 0.0060 |

> Despite low precision, anomaly detection models achieved **very high recall**, which is critical in real-world fraud detection where missing a fraud is costlier than a false alarm.

---

## Tech Stack

- Python
- Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
- Jupyter Notebook

---
