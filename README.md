# Wine Quality Prediction using Machine Learning

This project focuses on predicting wine quality based on physicochemical properties using multiple machine learning regression models. The main objective is to compare different algorithms, evaluate their performance, and analyze prediction errors in a structured and interpretable manner.

---

## Project Overview

Wine quality assessment is traditionally performed by human experts, which can be subjective and time-consuming. By leveraging machine learning, this project aims to build predictive models that estimate wine quality scores objectively using numerical features such as acidity, alcohol content, and sulfur dioxide levels.

The project covers the complete machine learning workflow:
- Data preprocessing
- Model training
- Model evaluation
- Error analysis
- Comparative analysis across models

---

## Dataset

- **Dataset**: Wine Quality Dataset
- **Target Variable**: `quality`
- **Features**: Physicochemical properties of wine
- **Type**: Regression problem with discrete target values

Preprocessing steps include:
- Handling outliers using the Interquartile Range (IQR) method with capping
- Feature scaling
- Train-test split

---

## Models Implemented

The following regression models are implemented and evaluated:

- Linear Regression
- Support Vector Regression (SVR)
- Random Forest Regressor
- K-Nearest Neighbors Regressor
- XGBoost Regressor

All models are trained using the same training and testing data splits to ensure fair comparison.

---

## Model Training

- Data split: 80% training, 20% testing
- Models are trained using default hyperparameters
- Training and evaluation are handled through modular and reusable functions

This approach allows easy experimentation with different models by simply changing the model key.

---

## Evaluation Metrics

Model performance is evaluated using standard regression metrics:

- **RMSE (Root Mean Squared Error)**
- **MSE (Mean Squared Error)**
- **MAE (Mean Absolute Error)**

In addition to continuous metrics, predictions are rounded to discrete quality values for deeper analysis.

---

## Prediction Error Analysis

The project includes detailed error analysis, such as:

- Identification of incorrect predictions only (correct predictions are excluded from logs)
- Absolute difference (`|Actual − Predicted|`) analysis
- Directional error analysis:
  - **Overestimation (Atas)**
  - **Underestimation (Bawah)**
- Per-class evaluation of correct vs incorrect predictions

This analysis helps in understanding not only how accurate the model is, but also *how and where* it makes mistakes.

---

## Results Summary

- Ensemble-based models (Random Forest and XGBoost) achieve the best performance overall
- Most prediction errors fall within a difference of ±1, indicating stable model behavior
- Random Forest shows consistent accuracy across multiple quality classes

Based on the evaluation results, **Random Forest Regressor** is selected as the final model for detailed analysis.

---

## 🗂 Project Structure
wine-quality-ml/<br>
├── data/<br>
│   └── winequality_processed.csv<br>
│   └── winequalityN.csv (Raw file)<br>
│   └── ...<br>
│<br>
├── notebooks/<br>
│   └── code.ipynb<br>
│   └── eda_raw.ipynb<br>
│   └── eda_preprocessed.ipynb<br>
│<br>
├── README.md<br>
├── png...<br>
└── requirements.txt


