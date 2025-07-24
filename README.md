# Autsim_Prediction
Austim _prediction using ML (Colab)
# Autism Spectrum Disorder Prediction

This project aims to predict Autism Spectrum Disorder (ASD) based on various factors using machine learning models.

## Table of Contents

- [Project Overview](#project-overview)
- [Data](#data)
- [Preprocessing](#preprocessing)
- [Model Training](#model-training)
- [Evaluation](#evaluation)
- [Installation](#installation)
- [Usage](#usage)

## Project Overview

The goal of this project is to build a classification model that can predict the likelihood of an individual having Autism Spectrum Disorder (ASD) based on a dataset containing various behavioral and demographic features. The project involves data loading, exploratory data analysis (EDA), preprocessing, model training, and evaluation.

## Data

The dataset used in this project is loaded from a CSV file named `train.csv`. It contains 22 columns, including demographic information, scores from an autism screening test (A1 to A10), and the target variable `Class/ASD` (0 for no ASD, 1 for ASD).

## Preprocessing

The following preprocessing steps were performed on the dataset:

- **Handling Missing Values:** Missing values in the 'ethnicity' and 'relation' columns were handled by replacing placeholder values with 'Others' and grouping similar categories.
- **Handling Outliers:** Outliers in the numerical columns ('age' and 'result') were identified and replaced with the median value of the respective columns using the Interquartile Range (IQR) method.
- **Label Encoding:** Categorical features were converted into numerical representations using Label Encoding. The fitted encoders were saved for future use.
- **Train-Test Split:** The dataset was split into training and testing sets to evaluate the model's performance on unseen data.
- **Handling Class Imbalance:** The training data was oversampled using the Synthetic Minority Over-sampling Technique (SMOTE) to address the class imbalance in the target variable.

## Model Training

Three tree-based classification models were trained and evaluated:

- Decision Tree
- Random Forest
- XGBoost

Cross-validation was used to assess the performance of these models with default parameters. Hyperparameter tuning was then performed using RandomizedSearchCV to find the best parameters for each model.

## Evaluation

The best-performing model (Random Forest in this case) was evaluated on the unseen test data. The evaluation metrics used include:

- Accuracy Score
- Confusion Matrix
- Classification Report (Precision, Recall, F1-score)

## Installation

To run this notebook, you need to have Python installed along with the following libraries:
