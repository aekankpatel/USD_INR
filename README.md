# USD to INR Exchange Rate Analysis

## Overview

This project analyzes the historical exchange rate of the US Dollar (USD) against the Indian Rupee (INR) using economic indicators such as inflation rates, trade balances, GDP growth, government effectiveness, and political stability. The analysis involves correlation studies and multiple linear regression modeling to identify factors influencing the exchange rate.

## Data Description

- **Source**: Dataset containing annual data for economic indicators.
- **Key Variables**:
  - **Conversion Rate**: USD to INR exchange rate.
  - **Inflation Rate**: Inflation rates of India and the USA.
  - **Trade Balance**: Trade balances of India and the USA.
  - **GDP Growth**: GDP growth rates of India, the USA, and globally.
  - **Government Effectiveness**: Governance quality in India and the USA.
  - **Political Stability**: Political stability indexes for India and the USA.
- **Format**: Excel file (`USD_INR.xlsx`).

## Analysis Steps

### 1. Data Loading and Overview
- The dataset is loaded into a Pandas DataFrame.
- The structure and summary statistics of the data are inspected to understand distributions and ranges of variables.

### 2. Correlation Analysis
- The correlation matrix highlights relationships between `Conversion Rate` and other variables:
  - Positive correlations:
    - `Political Stability of India` (0.828): Suggests that political stability in India increases the exchange rate.
  - Negative correlations:
    - `Government Effectiveness of USA` (-0.823): Indicates that better governance in the USA reduces the exchange rate.

### 3. Multiple Linear Regression
- A regression model is built to predict the `Conversion Rate` using:
  - Inflation rates, trade balances, GDP growth, government effectiveness, and political stability for both countries.
- **Key Findings**:
  - Significant predictors:
    - `Trade Balance of USA`: Positively impacts the exchange rate.
    - `GDP Growth of USA`: Positively impacts the exchange rate.
    - `Political Stability of India`: Positively impacts the exchange rate.
  - Non-significant predictors include `Inflation Rate of India` and `Government Effectiveness of USA`.

### 4. Model Performance
- **R-squared**: 94.6% of the variation in `Conversion Rate` is explained by the predictors.
- **Durbin-Watson**: Indicates minimal autocorrelation in residuals.
- **Condition Number**: High value suggests potential multicollinearity.

## How to Use
1. Load the `USD_INR.ipynb` notebook in Jupyter Notebook or JupyterLab.
2. Ensure the `USD_INR.xlsx` file is in the same directory.
3. Install required libraries: `pandas`, `numpy`, `statsmodels`, and `seaborn`.
4. Run the cells sequentially to execute the analysis and view results.

## Libraries Used
- **pandas**: For data manipulation and analysis.
- **numpy**: For numerical computations.
- **statsmodels**: For statistical modeling and regression.
- **seaborn**: For data visualization.
