
# Stock Market Data Analysis Project

## Overview

This project focuses on analyzing and predicting stock market data. It involves gathering real-time financial data from the Investors Exchange (IEX), conducting Exploratory Data Analysis (EDA), creating visualizations, and performing predictive analysis to evaluate risk and forecast future stock prices.

The main objectives are:
- Understanding the price changes of stocks over time
- Analyzing daily returns and their correlation between different stocks
- Visualizing stock data and calculating moving averages
- Estimating risk and predicting future stock price movements using Monte Carlo simulations

## Technologies Used
- **Python**: Main programming language
- **Libraries**: 
  - `pandas`: Data manipulation and analysis
  - `numpy`: Numerical operations
  - `matplotlib`, `seaborn`: Data visualization
  - `pandas_datareader`: For fetching stock data from IEX
  - `datetime`: For handling dates and times
  - `monte-carlo-simulation`: For predicting stock prices
- **IEX API**: For real-time stock data

## Steps and Methodology

### 1. Importing Libraries
We begin by importing essential libraries for data analysis and visualization, including `pandas`, `numpy`, `matplotlib`, and `seaborn`.

### 2. Data Collection
Stock data is fetched using the `pandas_datareader` library from the IEX API. For this project, we focus on four tech stocks: Apple (AAPL), Google (GOOG), Microsoft (MSFT), and Amazon (AMZN). The data is retrieved for the past year.

```python
tech_list = ['AAPL', 'GOOG', 'MSFT', 'AMZN']

3. Data Analysis
Price Changes: We explore the change in stock prices over time.
Daily Returns: The daily percentage returns of the stocks are calculated using pct_change().
Moving Averages: We compute various moving averages (10, 20, 50 days) to identify stock trends.
Correlation Analysis: We examine the correlation between stock prices and daily returns.
4. Data Visualization
Several visualizations are created to better understand the stock market data:
Stock Prices Over Time: Line plots to show the historical closing prices.
Stock Volume: Bar plots to visualize the trading volume.
Moving Averages: Plots comparing the closing prices with the moving averages.
5. Risk Analysis
Risk is assessed using:
Volatility: Standard deviation of daily returns.
Value at Risk (VaR): Various methods like the bootstrap and Monte Carlo simulations are used to estimate potential losses at a given confidence level.
6. Monte Carlo Simulation for Stock Prediction
Monte Carlo simulations are run to forecast future stock prices by simulating a large number of possible price paths based on geometric Brownian motion (GBM).
def monte_carlo_simulation(start_price, days, mu, sigma):
    # Function for Monte Carlo simulation
    # Returns simulated stock price over time

How to Use
Clone the Repository

 git clone https://github.com/yourusername/stock-market-analysis.git
cd stock-market-analysis


Install Dependencies

 Install the required Python libraries:

 pip install -r requirements.txt


Run the Script

 Run the Python script to fetch data, analyze it, and generate visualizations:

 python stock_analysis.py


Key Functions
Data Collection: Fetches stock data from the IEX API.
Moving Averages: Computes and visualizes moving averages for trend analysis.
Risk Analysis: Calculates daily returns and risk metrics such as standard deviation and Value at Risk (VaR).
Monte Carlo Simulation: Predicts future stock prices using random simulations.
Results
Visualizations: Plots for stock prices, volume, moving averages, and daily returns.
Risk Metrics: Value at Risk (VaR) for different stocks.
Predictions: Simulated future stock prices using Monte Carlo methods.

