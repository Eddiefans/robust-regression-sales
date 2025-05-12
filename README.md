# Sales Prediction using Linear Regression and XGBoost

This project explores sales prediction based on advertising data using two different models: Linear Regression and XGBoost. It demonstrates how addressing common statistical problems can improve model performance, particularly for linear models.

## Overview

Advertising spend across TV, radio, and newspaper channels is used to predict sales figures. The project compares a traditional statistical approach (Linear Regression) with a modern machine learning approach (XGBoost), before and after addressing data issues.

## Dataset

The dataset (`Advertising.csv`) contains:
- TV: Advertising dollars spent on TV
- Radio: Advertising dollars spent on Radio
- Newspaper: Advertising dollars spent on Newspaper
- Sales: Sales figures to predict

## Key Features

1. **Initial Model Training:** Training both models on raw data
2. **Regression Diagnostics:** Identifying six common linear regression problems:
   - Non-linearity
   - Correlated errors
   - Heteroscedasticity (non-constant variance)
   - Non-normality of residuals
   - Multicollinearity
   - High-leverage points and outliers

3. **Design Matrix Adjustments:** Addressing identified issues by:
   - Adding polynomial features for non-linear relationships
   - Log-transforming the target variable
   - Removing outliers and high-leverage points
   - Using Ridge regression for regularization
   - Adding interaction terms

4. **Model Retraining:** Evaluating performance improvements after adjustments

## Results

Before adjustments:
- Linear Regression: MSE = 3.17, R² = 0.90
- XGBoost: MSE = 0.39, R² = 0.99

After adjustments:
- Linear Regression: MSE = 1.05, R² = 0.953
- XGBoost: MSE = 0.50, R² = 0.977

## Findings

1. Addressing statistical assumptions significantly improved the linear model's performance
2. XGBoost performed slightly worse after the adjustments because:
   - It inherently handles non-linearities and outliers
   - Removing observations and transforming variables reduced information available to the model
   - Tree-based models already capture complex patterns automatically

3. This demonstrates an important difference between statistical and machine learning approaches:
   - Linear models: Require careful data preparation but offer better interpretability
   - Machine learning models: More robust to messy data but act more as black boxes

## Dependencies

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- statsmodels
- xgboost
- optuna

## How to Run

1. Ensure all dependencies are installed
2. Download the Advertising.csv dataset
3. Run the notebook cells sequentially

## Author

Eddie Aguilar Ceballos

## Date

May 12, 2025
