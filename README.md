# Disease Prediction Using Machine Learning

## 1. Project Overview
This project implements a machine-learning pipeline for binary disease prediction using the **Breast Cancer Wisconsin Diagnostic dataset** available through `scikit-learn`.

The goal is to classify breast-tumor observations as **malignant** or **benign** and compare three classification algorithms.

> **Educational note:** This project is for academic machine-learning practice only. It is not a medical diagnostic tool.

## 2. Dataset
- Source: `sklearn.datasets.load_breast_cancer`
- Samples: 569
- Input features: 30
- Classes: Malignant and Benign
- Train/test split: 80% / 20%
- Split method: stratified
- Random state: 42

## 3. Phase A — Data Preprocessing
1. Load the dataset directly from scikit-learn.
2. Separate input features (`X`) and target (`y`).
3. Check for missing values.
4. Use a stratified 80/20 train-test split.
5. Standardize features for Logistic Regression and SVM using pipelines.
6. Keep preprocessing inside the training pipeline to avoid data leakage.

## 4. Phase B — Models
The following models are implemented:
- Logistic Regression
- Random Forest
- Support Vector Machine (SVM)

## 5. Phase C — Evaluation
The following metrics are reported:
- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC

### Results
| Model | Accuracy | Precision | Recall | F1-score | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Logistic Regression | 0.9825 | 0.9861 | 0.9861 | 0.9861 | 0.9954 |
| SVM | 0.9825 | 0.9861 | 0.9861 | 0.9861 | 0.9950 |
| Random Forest | 0.9474 | 0.9583 | 0.9583 | 0.9583 | 0.9937 |

## 6. Result Interpretation
The models show strong predictive performance on the held-out test set. However, the metrics describe performance on this particular dataset and split; they should not be interpreted as evidence of clinical effectiveness.

For a medical application, additional validation on independent populations, calibration, clinical review, bias analysis, and appropriate regulatory evaluation would be required.

## 7. Repository Structure
```text
disease-prediction-ml/
│
├── disease_prediction_ml.ipynb
├── README.md
└── results/
    ├── model_metrics.csv
    ├── model_comparison.png
    ├── logistic_regression_confusion_matrix.png
    ├── random_forest_confusion_matrix.png
    └── svm_confusion_matrix.png
```

## 8. How to Run
Install the required packages:

```bash
pip install numpy pandas matplotlib scikit-learn jupyter
```

Then launch Jupyter:

```bash
jupyter notebook
```

Open `disease_prediction_ml.ipynb` and run the cells from top to bottom.

## 9. Assignment Requirements Covered
- [x] Publicly available disease dataset
- [x] Data preprocessing
- [x] 2–3 classification algorithms
- [x] Accuracy
- [x] Precision
- [x] Recall
- [x] F1-score
- [x] Additional metric: ROC-AUC
- [x] Commented Jupyter Notebook
- [x] README.md
- [x] Plots and figures in `results/`

## 10. Author
*Student:* Anika Ulfat<br>
*Course:* Federated Learning<br>
*Instructor:* M. A. Moyeen (Lecturer at IICT)
