# Bank Marketing Campaign Analysis: Predicting Term Deposit Subscriptions

This project focuses on analyzing a bank marketing campaign dataset to build a predictive model for identifying clients likely to subscribe to a term deposit. The goal is to leverage historical data to improve the efficiency and effectiveness of future marketing efforts.

## Project Overview

The project follows a standard data science pipeline, encompassing data loading, cleaning, exploratory data analysis (EDA), feature engineering, model building using XGBoost, model evaluation, and interpretation of results using SHAP and Gain metrics.

## Dataset

The dataset used in this project is related to direct marketing campaigns of a Portuguese banking institution. The marketing campaigns were based on phone calls. The target variable `y` indicates whether the client subscribed to a term deposit ('yes') or not ('no').

## Project Structure

The analysis is structured within a Google Colab notebook, covering the following key sections:

1.  **Data Loading and Initial Exploration**: Loading the dataset and performing initial checks.
2.  **Data Cleaning**: Handling missing values and preparing the data for analysis.
3.  **Exploratory Data Analysis (EDA)**: Visualizing and analyzing feature distributions, identifying relationships, and assessing target variable imbalance.
4.  **Feature Engineering and Preprocessing**: Creating new features and preparing the data for the predictive model (scaling numerical features, encoding categorical features).
5.  **Model Building and Evaluation**: Building an XGBoost classification model and evaluating its performance using appropriate metrics for imbalanced datasets (Precision, Recall, F1-score, ROC AUC).
6.  **Model Interpretation**: Understanding feature importance using SHAP and Gain metrics to explain the model's predictions.

## Key Findings

*   The target variable (term deposit subscription) is highly imbalanced, with a significantly lower number of subscribers compared to non-subscribers.
*   Economic indicators (`nr.employed`, `euribor3m`, `emp.var.rate`) were identified as the most influential features in predicting subscriptions.
*   The outcome of previous marketing campaigns (`poutcome_success`) is a strong predictor of future subscription.
*   The month of contact and the contact type (`contact_cellular`) significantly impact the subscription rate.

## Model Performance

The XGBoost model achieved an overall accuracy of 84.2%. However, due to class imbalance, other metrics provide a more insightful evaluation:

*   **Precision (Class 1 - Yes):** 37.6%
*   **Recall (Class 1 - Yes):** 60.8%
*   **F1-score (Class 1 - Yes):** 0.465
*   **ROC AUC Score:** 0.787

The model demonstrates reasonable discriminative power (AUC), but precision for the positive class is an area for potential improvement, indicating a notable number of false positives.

## Getting Started

To replicate this analysis:

1.  Clone the repository.
2.  Open the Google Colab notebook.
3.  Ensure you have access to the `bank-additional-full.csv` dataset, located at `/content/drive/MyDrive/Colab Notebooks/data/`. You may need to adjust the file path if your data is stored elsewhere.
4.  Run the notebook cells sequentially.

## Dependencies

The following libraries are required to run the notebook:

*   pandas
*   numpy
*   scikit-learn
*   xgboost
*   matplotlib
*   seaborn
*   ydata-profiling
*   shap

These can be installed using pip:
