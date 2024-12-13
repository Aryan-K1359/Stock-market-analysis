
# Stock Market Analysis

This project focuses on analyzing stock market data for tech companies and performing risk analysis and predictions using Monte Carlo simulations.

## Tech Companies
The analysis includes stock data for the following companies:
- AAPL (Apple)
- GOOG (Google)
- MSFT (Microsoft)
- AMZN (Amazon)

## 3. Data Analysis
### Price Changes
We explore the change in stock prices over time.

### Daily Returns
The daily percentage returns of the stocks are calculated using `pct_change()`.

### Moving Averages
We compute various moving averages (10, 20, 50 days) to identify stock trends.

### Correlation Analysis
We examine the correlation between stock prices and daily returns.

## 4. Data Visualization
Several visualizations are created to better understand the stock market data:
- **Stock Prices Over Time:** Line plots to show the historical closing prices.
- **Stock Volume:** Bar plots to visualize the trading volume.
- **Moving Averages:** Plots comparing the closing prices with the moving averages.

## 5. Risk Analysis
Risk is assessed using:
- **Volatility:** Standard deviation of daily returns.
- **Value at Risk (VaR):** Various methods like the bootstrap and Monte Carlo simulations are used to estimate potential losses at a given confidence level.

## 6. Monte Carlo Simulation for Stock Prediction
Monte Carlo simulations are run to forecast future stock prices by simulating a large number of possible price paths based on geometric Brownian motion (GBM).

### Code Example:
```python
def monte_carlo_simulation(start_price, days, mu, sigma):
    # Function for Monte Carlo simulation
    # Returns simulated stock price over time
```


```

## Key Functions
- **Data Collection:** Fetches stock data from the IEX API.
- **Moving Averages:** Computes and visualizes moving averages for trend analysis.
- **Risk Analysis:** Calculates daily returns and risk metrics such as standard deviation and Value at Risk (VaR).
- **Monte Carlo Simulation:** Predicts future stock prices using random simulations.

## Results
- **Visualizations:** Plots for stock prices, volume, moving averages, and daily returns.
- **Risk Metrics:** Value at Risk (VaR) for different stocks.
- **Predictions:** Simulated future stock prices using Monte Carlo methods.
```

