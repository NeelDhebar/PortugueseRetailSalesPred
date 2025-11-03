# Sales Prediction Model

This project uses machine learning to predict daily sales based on store data, pricing, and stock levels.
The dataset contains historical sales information from a Portuguese retailer, and the goal is to forecast sales more accurately using engineered time-based features.

## Dataset
The dataset includes the following columns:

- **date** - Date of record
- **sales** - Number of units sold
- **stock** - Stock available
= **price** - Price of the product

Column names were translated to English for consistency.

## Feature Engineering

Several new features were created to help capture temporal and behavioural patterns:

- **is_weekend** - Binary flag for weekend days
- **sales_lag_7** - Sales value from 7 days earlier
- **sales_rolling_7** - 7-day rolling mean of sales
- **price_change** - Day-to-day percentage of change in price
- **stock_to_sales_ratio** - Ratio of stock to recent sales

Missing or infinite values were handled and cleaned prior to training.

## Models Used
1. **Linear Regression**
2. **Polynomial Regression**
3. **Ridge Regression**

All models were trained and evaluated using a **sequential 80:20 time-based split**, ensuring no data leakage from future values.

## Libraries Used
- pandas
- numpy
- scikit-learn
- matplotlib