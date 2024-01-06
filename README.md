# Google Stock Price Prediction with Facebook Prophet

## Overview

This Python script utilizes Facebook Prophet to predict the closing stock prices for Google incorporation based on the provided dataset "google-data.csv" spanning from 2013 to 2018. The script involves data preprocessing, hyperparameter tuning using Bayesian Optimization, model training, and performance evaluation. The goal is to forecast stock prices for the next 100 days.

## Dataset Information

### Description

The dataset represents the Stock Price of Google incorporation between 2013-2018 years. The data is presented in CSV format with columns: Date, Open, High, Low, Close, Volume, and Adj Close.

### File

- **Dataset:** [google-data.csv]

## Script Structure

### 1. Data Loading and Preprocessing

- **Loading Data:** The script loads the dataset into a Pandas DataFrame and performs initial checks for missing values and duplicates.

- **Interpolation:** Missing values in relevant columns are interpolated using the quadratic method.

### 2. Model Training with Hyperparameter Tuning

- **Prophet Model:** A Prophet model is trained with hyperparameters tuned using Bayesian Optimization. The parameters include changepoint_prior_scale, n_changepoints, holidays_prior_scale, seasonality_mode, and yearly_seasonality.

- **Tuning Process:** The script iterates through a predefined parameter grid, trains Prophet models with different sets of hyperparameters, and evaluates their Mean Percentage Error (MPE) on the training set.

- **Best Parameters:** The script selects the set of hyperparameters with the lowest MPE for the final model.

### 3. Forecasting

- **Making Forecasts:** The final Prophet model is used to make forecasts for the next 100 days.

### 4. Model Evaluation

- **Cross-Validation:** The script performs cross-validation to evaluate the model's performance over time.

- **Performance Metrics:** Various performance metrics, including Mean Absolute Percentage Error (MAPE), are calculated and displayed.

### 5. Visualization

- **Plotting Results:** The script visualizes the predicted stock prices for the next 100 days and displays relevant diagnostic plots.

## How to Use

1. Ensure you have Python installed along with the required libraries specified in the script (Prophet, Pandas, NumPy, Matplotlib).

2. Place the "google-data.csv" dataset in the same directory as the script.

3. Run the script in a Python environment, considering any specific package dependencies.

## Author

- **Author:** Ilaha Musayeva
- **Date:** 10/20/2023


