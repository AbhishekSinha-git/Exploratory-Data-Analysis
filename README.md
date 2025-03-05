# Exploratory-Data-Analysis
=======
Nifty 50 Portfolio Analysis Project
Overview
This project performs a comprehensive financial analysis of the Nifty 50 stocks, including data retrieval, returns calculation, portfolio risk assessment, and beta computation.
Project Structure

Data retrieval of Nifty 50 stocks from Yahoo Finance
Calculation of daily stock returns
Portfolio risk and return analysis
Beta computation for individual stocks

Prerequisites
Required Libraries

yfinance: For downloading stock price data
numpy: For numerical computations
pandas: For data manipulation
os: For directory and file operations

Installation
bashCopypip install yfinance numpy pandas
Code Breakdown
1. Stock Data Retrieval

Fetches historical stock data for all Nifty 50 stocks from 2000-01-01 to 2021-04-30
Saves individual stock data as Excel files in nifty50_data directory

2. Returns Computation
The StockReturnsComputing() function calculates daily percentage returns for each stock using the formula:
CopyReturn = ((Price[t+1] - Price[t]) / Price[t]) * 100
3. Beta Calculation
Beta measures a stock's volatility relative to the market:

Computed as the covariance of stock returns with market returns divided by market variance
Indicates stock's sensitivity to market movements

β > 1: More volatile than market
β = 1: Moves with market
β < 1: Less volatile than market



4. Portfolio Analysis
Computes key portfolio metrics:

Annualized Risk (Portfolio Volatility): Measure of portfolio return variability
Annualized Return: Expected yearly portfolio performance
Portfolio Beta: Aggregate beta of all stocks in the portfolio

Example Output
pythonCopyannualizedRisk = 14.69%
annualizedReturn = 11.99%
portfolioBeta = 1.00
Key Financial Metrics Explained
1. Mean Returns

Average percentage return for each stock
Indicates typical daily performance

2. Variance-Covariance Matrix

Measures return variability and interdependencies between stocks
Critical for understanding portfolio risk

3. Portfolio Weights

Equal weights assigned to all stocks (1/n strategy)
Represents a simple diversification approach

Limitations

Uses historical data (2000-2021)
Assumes equal weighting
Does not account for transaction costs or taxes

Future Improvements

Implement dynamic weight allocation
Add risk-adjusted return metrics
Include more recent data

License
[Choose an appropriate license, e.g., MIT]
Contributing
Contributions, issues, and feature requests are welcome!
