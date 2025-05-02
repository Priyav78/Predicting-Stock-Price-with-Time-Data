# Stock-Prediction-with-Time-Data
Predicting stock prices from historical data.
Stock Price Forecasting using Time Series Regression

This project builds and evaluates models to predict stock closing prices based on historical stock price data and company metadata. The models are trained on a cleaned and merged dataset from the S&P 500 stocks.

📊 Objective

To predict the next day's closing stock price using lag features and rolling averages derived from historical data.

📁 Dataset

sp500_companies.csv: Company metadata including sector, industry, market cap, etc.

historical_prices.csv: Daily stock prices including Open, Close, High, Low, Volume, Date, and Symbol

Source: Kaggle - S&P 500 Stocks

🧱 Features Used

Close_lag1: Previous day's closing price

Close_lag7: Closing price from 7 days ago

Close_roll3: 3-day rolling average of closing prices

🧰 Models Compared

Linear Regression

Random Forest Regressor

XGBoost Regressor

Note: Hyperparameter tuning (e.g., GridSearchCV) is commented out to preserve memory. Plain versions of each model were used instead.

🔢 Results

Model

RMSE

R² Score

Linear Regression

1.88

0.9997

Random Forest

Pending (long runtime)

XGBoost

13.50

0.9831

Linear Regression performed best due to the strong linear relationships in the time-series features.

🪑 Business Application

Companies can use this model to:

Forecast stock price trends for portfolio management

Drive risk models and stop-loss triggers

Support internal trading signals or research

✅ Forecasting Example

To make a future prediction:

Collect the most recent 7 days of closing prices.

Calculate:

Close_lag1

Close_lag7

Close_roll3

Input them into the trained model:

model.predict([[close_lag1, close_lag7, close_roll3]])

📚 Author

Priya VermaBoston University
M.S. in Data Science

🔧 Tools Used

Python

Pandas, NumPy, Seaborn, Matplotlib

Scikit-learn, XGBoost

Jupyter Notebook
