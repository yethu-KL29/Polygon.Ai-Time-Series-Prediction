# Stock Price Prediction using Support Vector Regression (SVR)

This project focuses on predicting stock prices using the **Support Vector Regression (SVR)** model. The goal is to use historical stock data and various engineered features to forecast future stock prices.

## Table of Contents
- [Project Overview](#project-overview)
- [Methodology](#methodology)
- [Evaluation](#evaluation)
- [Visualizations](#visualizations)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [License](#license)

## Project Overview

This project uses historical stock data (e.g., open, close, high, low, volume) to build a model that predicts stock prices. The model uses **Support Vector Regression (SVR)** with a **Radial Basis Function (RBF)** kernel for time series forecasting. We engineered additional features like **moving averages**, **price changes**, and **volatility** to improve the model's performance.

### Key Features:
- **Stock Data**: Historical stock prices including open, close, high, low, and volume.
- **Features Engineered**: Price change, log returns, moving averages (7-day, 14-day, 30-day), and volatility.
- **Model**: Support Vector Regression (SVR) with hyperparameter tuning.
- **Performance Metrics**: Mean Squared Error (MSE), Root Mean Squared Error (RMSE), R² Score.

## Methodology

1. **Data Preprocessing**:
   - Filled missing values using the mean of the respective columns.
   - Scaled the features using **StandardScaler** to normalize the data.

2. **Model Development**:
   - Used **Support Vector Regression (SVR)** with the **RBF kernel**.
   - Optimized the model using **GridSearchCV** for hyperparameter tuning, including `C`, `epsilon`, and `gamma`.

3. **Evaluation**:
   - The model's performance was evaluated using **Mean Squared Error (MSE)**, **Root Mean Squared Error (RMSE)**, and **R² Score**.

## Evaluation

The model achieved an **R² score of 0.96**, indicating that **96%** of the variance in stock prices was explained by the model. The **MSE** of **3.09** and **RMSE** of **1.76** suggest that the model's predictions are reliable with minimal error.

## Visualizations

- **Actual vs Predicted Prices**: A line plot comparing the predicted stock prices with actual values.
- **Residual Distribution**: A distribution plot of residuals to evaluate model performance.
- **Moving Average**: A plot of 7-day moving averages to capture market trends.
- **Correlation Plot**: Visualized the correlation between different features to understand their relationships.
- **Pairplot**: Observed pairwise relationships between features to identify patterns and dependencies.

## Requirements

To run this project, you'll need the following libraries:

- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- statsmodels (for time series decomposition)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/stock-price-prediction.git
