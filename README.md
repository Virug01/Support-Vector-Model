# Support Vector Regression on Insurance Dataset

This project demonstrates the application of Support Vector Regression (SVR) to predict insurance charges based on various features. It covers data cleaning, feature engineering, exploratory data analysis, and model evaluation.

## Table of Contents

- [Introduction](#introduction)
- [Installation](#installation)
- [Data Description](#data-description)
- [Data Cleaning](#data-cleaning)
- [Feature Engineering](#feature-engineering)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Modeling](#modeling)
- [Results](#results)
- [Conclusion](#conclusion)

## Introduction

The goal of this project is to predict insurance charges using Support Vector Regression. We preprocess the data, perform exploratory data analysis, and build a regression model to make predictions.

## Installation

To run this project, you need to have Python installed along with the following libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

## Data Description

The dataset used in this project is `insurance.csv`. It includes the following columns:

- `age`: Age of the primary beneficiary
- `sex`: Gender of the beneficiary (male, female)
- `bmi`: Body mass index
- `children`: Number of children/dependents covered by health insurance
- `smoker`: Smoking status (yes, no)
- `region`: Residential area in the US (northeast, southeast, southwest, northwest)
- `charges`: Individual medical costs billed by health insurance

## Data Cleaning

Data cleaning steps include:

1. **Handling Missing Values**: Ensure there are no missing values in the dataset.
2. **Encoding Categorical Variables**: Convert categorical variables such as `sex`, `smoker`, and `region` into numerical values using one-hot encoding.

## Feature Engineering

Feature engineering steps include:

1. **Combining DataFrames**: Combine the original dataframe with the new encoded columns.
2. **Renaming Columns**: Rename columns for better readability.
3. **Dropping Unnecessary Columns**: Drop original categorical columns after encoding.

## Exploratory Data Analysis

We perform EDA to understand the relationships between features and insurance charges:

- **Count Plots**: Visualize the distribution of `sex`.
- **Box Plots**: Analyze the distribution of `charges` across different `sex` and `smoker` categories.
- **Scatter Plots**: Examine the relationships between `age`, `bmi`, and `charges`.
- **Correlation Heatmap**: Display correlations between different features.

## Modeling

We implement Support Vector Regression (SVR) using the following steps:

1. **Splitting Data**: Split the data into training and testing sets using `train_test_split`.
2. **Scaling Data**: Standardize the features using `StandardScaler`.
3. **Training the Model**: Fit the `SVR` model on the training data.
4. **Making Predictions**: Predict the insurance charges for the test data.
5. **Evaluating the Model**: Calculate mean absolute error (MAE) and mean squared error (MSE) to evaluate the model's performance.

## Results

The evaluation metrics for the SVR model are as follows:

- **Mean Absolute Error (MAE)**: `7927.66`
- **Mean Squared Error (MSE)**: `155000203`
- **Root Mean Squared Error (RMSE)**: `12449.907`

## Conclusion

In this project, we implemented Support Vector Regression to predict insurance charges. The model was evaluated using MAE, MSE, and RMSE, and the results indicate its performance on the test data.
