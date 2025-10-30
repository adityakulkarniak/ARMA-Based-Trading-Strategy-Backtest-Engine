# ARMA-Based-Trading-Strategy-Backtest-Engine
This project presents a rigorous backtesting framework to investigate short-term predictability in financial asset returns. It moves beyond simplistic "buy-and-hold" strategies by implementing a rolling-forecast trading algorithm based on an $ARMA(p,q)$ model.

 ARMA: A Backtest EngineCan we find signal in the noise? This project tests if $ARMA(p,q)$ time series models can actually predict stock market chop.No hype, just a rigorous backtest simulation. 

 This script runs an expanding-window forecast to simulate a real-world trading scenario.

Ingest: Grabs price data from yfinance ($AAPL).Transform: Converts prices to stationary returns (.pct_change()).Model: At each new day $t$, the $ARMA$ model re-trains on all data up to $t-1$.

Forecast: Predicts the return for day $t$.Execute:IF pred > thresh  BUY.Hold for 1 day, then SELL.

