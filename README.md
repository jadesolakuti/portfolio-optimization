# Portfolio Optimization Project

This project is a Python-based portfolio optimizer that calculates **expected returns**, **portfolio risk (volatility)**, and **Sharpe ratios** for multiple assets using historical data. It applies **Modern Portfolio Theory (MPT)** to find the optimal allocation of a portfolio under constraints.

- **Data sources:** Yahoo Finance (`yfinance`) for historical stock prices, FRED API for the U.S. 10-year Treasury yield (risk-free rate).  
- **Features:** 
  - Compute log returns, covariance matrix, portfolio variance
  - Optimize portfolio weights to maximize Sharpe ratio
  - Visualize optimal portfolio allocation
- **Technologies:** Python, NumPy, Pandas, Matplotlib, SciPy, yfinance, fredapi

**How to run:**
1. Clone the repository and activate your virtual environment.
2. Install dependencies with `pip install -r requirements.txt`.
3. Edit the `tickers` list to your preferred assets.
4. Run the Python script to get optimal weights, expected return, volatility, and Sharpe ratio, along with a bar chart of allocations.

This project demonstrates applied **quantitative finance** and **data analysis** skills, useful for portfolio management and financial modeling.
