# Stock Market Data Analysis Report

## Introduction
The Stock Market Data Analysis project explores financial data from the stock market to gain insights into stock performance, risk, and predictive modeling. This report leverages real-time data obtained from The Investors Exchange (IEX) using Python libraries such as Pandas, Matplotlib, and Seaborn. The goal is to analyze the historical performance of stocks, examine risk factors, and use statistical methods, including the Monte Carlo method, to predict future stock prices.

## Objective
The main objectives of this project include answering the following questions:
- What was the change in the price of the stock over time?
- What was the average daily return of the stock?
- What was the moving average of the stocks?
- What was the correlation between different stocks' closing prices?
- How much value is at risk by investing in a particular stock?
- How can we predict future stock behavior using statistical methods?

## Data Collection
The data for the analysis is obtained using the **iexfinance** Python library from The Investors Exchange (IEX). For this analysis, stock data for four technology companies—Apple (AAPL), Google (GOOG), Microsoft (MSFT), and Amazon (AMZN)—is retrieved for the past year. The data includes stock attributes such as the opening price, closing price, highest and lowest price, and trading volume.

## Stock Data Analysis

### Basic Analysis
We began by reviewing basic stock attributes like the open, high, low, close prices, and volume. For example, Apple’s stock data shows various statistics such as the average closing price of $187.61 and a standard deviation of $20.68 over the year analyzed.

#### Summary Statistics:
- **Mean Close Price for AAPL**: $187.61
- **Standard Deviation of Close Price**: $20.68
- **Maximum Close Price**: $232.07
- **Minimum Close Price**: $153.39

#### Data Visualizations
- **Closing Price Trend**: A plot of the closing price of Apple over the year showed fluctuations, with notable peaks and dips.
- **Volume Traded**: A plot showing the volume traded each day helped us identify periods of high trading activity.

### Moving Average
The moving average (MA) is a key technical indicator used to smooth out price data. We calculated moving averages for 10, 20, and 50 days for Apple’s stock and plotted these alongside the actual closing prices. Moving averages help identify trends and potential reversal points in stock prices.

### Daily Return Analysis
The daily return represents the percentage change in the stock price from one day to the next. We calculated the daily return for Apple’s stock and plotted it to identify periods of high volatility.

- **Average Daily Return**: A negative or positive daily return reflects the volatility of the stock. For Apple, the daily returns were mostly concentrated around small positive and negative changes.

#### Histogram of Daily Returns
The histogram for Apple’s daily returns showed a fairly normal distribution, with most returns clustered around the mean.

### Correlation Analysis
We analyzed the correlation between the daily returns of the stocks in the portfolio (AAPL, GOOG, MSFT, AMZN). A pairplot was used to visualize the relationships between the stocks' daily returns, which provided insights into how similarly the stocks moved during the analyzed period.

- **Google vs Microsoft Correlation**: A scatter plot showed that Google and Microsoft had a moderately positive correlation in their daily returns.
- **Pairwise Correlation**: We calculated the Pearson correlation for each pair of stocks to assess how closely their daily returns were correlated.

#### Correlation Heatmap
A heatmap was used to visualize the correlations between daily returns of the stocks. This helped to understand the strength and direction of relationships between the stocks.

## Risk Analysis

### Quantifying Risk
Risk is a critical component of stock market analysis. We calculated the risk of each stock using the standard deviation of daily returns, which represents the volatility of the stock. A scatter plot was generated to visualize the relationship between the expected return (mean daily return) and the risk (standard deviation) for each stock.

#### Value at Risk (VaR)
Value at Risk (VaR) quantifies the potential loss in the value of an investment over a given time period with a certain level of confidence. We used the bootstrap method and the Monte Carlo simulation to calculate VaR for Apple’s stock.

- **Bootstrap Method**: The empirical quantile of daily returns at the 5% level was calculated, indicating that with 95% confidence, Apple’s worst daily loss would not exceed 2.4%.
  
- **Monte Carlo Simulation**: Using a Geometric Brownian Motion (GBM) model, we simulated future stock prices and calculated the potential losses under random market conditions. The Monte Carlo method provided a stochastic process for predicting stock price behavior and risk.

### Monte Carlo Simulation Results
The Monte Carlo simulation showed multiple possible price paths for Apple’s stock based on historical volatility and expected returns. This method demonstrated the potential for both upward and downward movement in stock prices over the next year.

## Conclusion
The analysis provides valuable insights into the behavior and risks associated with technology stocks. The findings include:
- Moving averages provide useful trends for identifying potential buy or sell points.
- Daily returns analysis helps assess the volatility of the stock.
- Correlation analysis identifies how stocks in a portfolio move together, assisting in diversification decisions.
- Risk analysis, including Value at Risk and Monte Carlo simulations, helps estimate potential losses under different market conditions.

This report demonstrates the power of data analysis techniques such as moving averages, correlation analysis, and Monte Carlo simulations in predicting and understanding stock market behavior. These tools are crucial for making informed investment decisions.
