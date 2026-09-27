# Disease Prediction Using Machine Learning — Assignment Report

**Student:** Anika Ulfat Easha  
**Dataset:** Breast Cancer Wisconsin Diagnostic Dataset  
**Task:** Binary disease classification

## 1. Introduction

Machine learning can be used to classify medical observations into disease-related categories based on measurable features. This assignment implements a complete machine-learning workflow using the Breast Cancer Wisconsin Diagnostic dataset from scikit-learn. The objective is to classify tumor observations as malignant or benign and compare three machine-learning algorithms.

## 2. Dataset

The dataset contains 569 observations and 30 numerical input features. The target has two classes: malignant and benign. The dataset is loaded directly using `sklearn.datasets.load_breast_cancer`.

## 3. Preprocessing

The preprocessing workflow includes:

1. Loading the dataset.
2. Separating features and target labels.
3. Checking the dataset for missing values.
4. Splitting the data into 80% training and 20% testing sets using stratification.
5. Standardizing features for Logistic Regression and SVM using scikit-learn pipelines.
6. Keeping preprocessing within the training pipeline to reduce the risk of data leakage.

## 4. Models

Three classification algorithms were implemented:

- Logistic Regression
- Random Forest
- Support Vector Machine (SVM)

These models provide different learning approaches: a linear probabilistic classifier, an ensemble of decision trees, and a margin-based classifier.

## 5. Evaluation Metrics

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC

Confusion matrices and a model-comparison plot are also included in the `results/` directory.

## 6. Results

| Model | Accuracy | Precision | Recall | F1-score | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Logistic Regression | 0.9825 | 0.9861 | 0.9861 | 0.9861 | 0.9954 |
| SVM | 0.9825 | 0.9861 | 0.9861 | 0.9861 | 0.9950 |
| Random Forest | 0.9474 | 0.9583 | 0.9583 | 0.9583 | 0.9937 |

## 7. Discussion

All three models achieved strong performance on the held-out test set. Logistic Regression and SVM produced the same accuracy, precision, recall, and F1-score for this particular split, while their ROC-AUC values were also very close. Random Forest produced lower scores on this test split but still showed strong classification performance.

These results are specific to the selected dataset, preprocessing procedure, random split, and model settings. They should not be interpreted as evidence that these models are ready for clinical use.

## 8. Conclusion

This assignment demonstrates the complete machine-learning workflow required for a disease-prediction classification problem: dataset loading, preprocessing, model implementation, metric-based evaluation, visualization, and result interpretation. The project satisfies the required use of multiple models and evaluation metrics and provides reproducible code in a Jupyter Notebook.

## 9. Ethical and Practical Note

This is an academic machine-learning project. The model is **not a medical diagnostic system**. Real clinical deployment would require independent external validation, clinical assessment, calibration, fairness/bias analysis, data governance, and applicable regulatory review.
