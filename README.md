# ML-driven-Monte-Carlo-Value-At-Risk
Forecasting portfolio risk by combining a machine-learning volatility model with a Monte Carlo simulation engine.

# Overview
Download daily prices for a 4-stock equal-weight portfolio (AAPL, MSFT, JPM, XOM).
Engineer features: lagged returns, absolute returns, 5/21/63-day rolling volatility.
Train a Random Forest to forecast next-5-day portfolio volatility (time-ordered 70/30 split, no shuffling).
Simulate 5,000 portfolio returns per day using correlated Student-t shocks (Cholesky), scaled to the ML volatility forecast.
Compute 95% VaR and CVaR.
Backtest out-of-sample against a naive 21-day rolling-volatility benchmark, validated with the Kupiec POF test.
