# Prediction-of-S-P500-in-R


# README for Stock Market Analysis in R

## Introduction

This project focuses on analyzing the stock market data using various statistical and machine learning techniques in R. The dataset used is `Smarket`, which contains daily percentage returns for the S&P 500 index over a period of several years. The analysis includes data visualization, statistical summaries, logistic regression, and regularization methods like Ridge and Lasso.

## Prerequisites

Before running the code, ensure that you have the following libraries installed:

```R
install.packages("ISLR2")
install.packages("ggplot2")
install.packages("glmnet")
install.packages("pROC")
```

You can load the required libraries with:

```R
library(ISLR2)
library(ggplot2)
library(glmnet)
library(pROC)
```

## Data Exploration

1. **View the First Few Rows**: The first six rows of the `Smarket` dataset are displayed using the `head(Smarket)` function.
2. **Summary Statistics**: Summary statistics of the dataset are generated using `summary(Smarket)`.
3. **Volume and Price Analysis**: Various plots are created to visualize trends in `Volume`, `Today`, and `Direction` over the years.

## Data Visualization

1. **Scatter Plots**: Scatter plots are created using base R and `ggplot2` to visualize the relationship between `Today`, `Volume`, and `Direction`.
2. **Boxplots and Histograms**: These are used to understand the distribution of `Today` and other `Lag` variables.
3. **Bar Plots**: Used to visualize the frequency of data points by year and direction.

## Correlation Analysis

Correlation matrices are calculated to study the relationship between various quantitative variables, excluding qualitative ones.

## Data Selection and Filtering

The code includes examples of how to:

- Select specific rows and columns.
- Filter data based on conditions (e.g., specific years or price movements).
- Select every nth row.

## Logistic Regression

1. **Model Fitting**: A logistic regression model is fitted to predict the `Direction` (Up/Down) based on lag variables.
2. **Model Evaluation**: The performance of the logistic regression model is evaluated by comparing predicted values with actual values.

## Ridge and Lasso Regression

1. **Model Fitting**: Ridge and Lasso regression models are fitted using the `glmnet` package.
2. **Cross-Validation**: Cross-validation is used to find the optimal lambda for both Ridge and Lasso.
3. **Model Evaluation**: The Root Mean Squared Prediction Error (rMSPE) is calculated for out-of-sample predictions.

## Model Training and Testing

1. **Data Splitting**: The data is split into training and test sets based on the year (before and after 2005).
2. **Ordinary Least Squares (OLS)**: An OLS regression model is fitted to the training data, and predictions are made on the test data.

## Output

1. **Plot Saving**: The code demonstrates how to save plots as PNG and PDF files using `ggsave`.
2. **Coefficients and Predictions**: The code outputs the coefficients of the models and calculates prediction errors.

## How to Run the Code

1. Load the required libraries.
2. Run the code snippets sequentially to perform data exploration, model fitting, and evaluation.
3. Adjust the code to suit your specific analysis needs (e.g., changing the years for training/testing or the variables used in models).

## Conclusion

This analysis provides a comprehensive overview of the S&P 500 index data using statistical and machine learning techniques. The project demonstrates the process of model building, from initial data exploration to advanced regularization methods like Ridge and Lasso regression.
