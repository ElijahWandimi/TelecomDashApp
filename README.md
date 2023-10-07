# Telecom Churn Prediction Project

## Overview

This project aims to predict customer churn in a telecom company using machine learning techniques. Churn prediction is a critical task for businesses to understand and retain their customer base.

## Data

The dataset used in this project is sourced from a telecom company and includes information about various aspects of customer interaction with their services. The dataset has 5986 entries and 22 columns, including features such as customer demographics, service usage, contract details, and payment information.

### Data Preprocessing

- Unnecessary columns (`Unnamed: 0` and `customerID`) were dropped from the dataset.
- Categorical columns were converted to the 'category' data type to prepare the data for machine learning modeling.
- Descriptive statistics of numerical columns (`SeniorCitizen`, `tenure`, `MonthlyCharges`) were provided.

## Exploratory Data Analysis (EDA)

The EDA section explores the distribution and relationships of different features in the dataset.

### Customer Demographics

- The gender distribution of customers was visualized concerning churn.
- The distribution of senior citizens and their relation to churn was explored.
- The impact of partnership (marriage) on churn was visualized.
- The presence of dependents and its correlation with churn was investigated.

### Contract and Service Usage

- The types of contracts (Month-to-month, Two years, One year) were explored, revealing a majority of month-to-month contracts.
- The overall balance of churn in the dataset was visualized.
- The tenure of customers was analyzed in relation to churn.
- Payment methods and their association with churn were examined.

## Modelling

### Data Encoding and Splitting

- Categorical features were encoded using label encoding.
- The dataset was split into training and validation sets.

### CatBoost Model

- A CatBoostClassifier was used for modeling, as it inherently handles categorical features without explicit encoding.
- The model was trained on the training set and evaluated on the validation set.
- Evaluation metrics such as ROC AUC score, F1 score, and classification report were provided.

### Feature Importance

- The feature importance of the model was visualized using a horizontal bar chart.
- SHAP (SHapley Additive exPlanations) values were calculated and visualized to understand the impact of each feature on the model's predictions.

## Results and Conclusion

- The trained model achieved a ROC AUC score of approximately 0.676 and an F1 score of 0.517 on the validation set.
- The classification report provides a detailed breakdown of precision, recall, and F1 score for both classes (churn, non-churn).
- Feature importance analysis reveals the most influential features in predicting customer churn.

## Recommendations

- Based on the analysis, the company can focus on improving customer retention strategies, especially for customers with characteristics associated with higher churn rates.
- Further model refinement and tuning could potentially enhance predictive performance.

## Dependencies

- The project relies on various Python libraries, including pandas, matplotlib, numpy, seaborn, scikit-learn, catboost, and shap.

## Usage

- The code provided in the repository can be used for further exploration, refinement, and adaptation for similar churn prediction projects.
