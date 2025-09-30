API key for Fred = 474454b35638670b136ca852f45b70d1

# minimize(...) comes from scipy.optimize.
# Its job: find values of variables (here, portfolio weights) that minimize a function.
# Since optimization algorithms usually minimize by default I minimized the negative Sharpe ratio instead.
# That’s why the function is neg_sharpe_ratio.

# initial_weights - This is the starting point for the optimizer.
# Example: If you have 3 stocks, you might start with [0.33, 0.33, 0.34].
# The algorithm will then tweak these values to search for better ones.

# args=(log_returns, cov_matrix, risk_free_rate) - These are extra inputs passed into the neg_sharpe_ratio function.
# When minimize calls neg_sharpe_ratio(weights, log_returns, cov_matrix, risk_free_rate), it tries different weights but keeps the other values fixed:
# log_returns = matrix of historical returns
# cov_matrix = covariance matrix of returns (used for risk calculation)
# risk_free_rate = safe benchmark return

# method='SLSQP'
# This means Sequential Least Squares Quadratic Programming.
# A common algorithm for portfolio optimization because it handles both bounds and constraints well
# and it works with smooth functions like variance.

# optimized_results
# The output object returned by minimize.
# It contains useful info:
# optimized_results.x → the optimized weights
# optimized_results.fun → the minimized value (here, the negative Sharpe)
# optimized_results.success → whether optimization worked

# In plain finance terms:
# This line is where the computer takes your equal-weight portfolio, 
# and systematically adjusts the allocations 
# (under the rules you gave: weights between 0–1 and must sum to 1) 
# until it finds the portfolio with the highest risk-adjusted return (Sharpe ratio).
