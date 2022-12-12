Type: #atom
Atom: [[Time Series Models - Forecasting & StatArb (J)]]
Topic: Quant 
Understanding: #Exploratory 

----
# Overview

In this notebook, Jansen performs stat arb on cointegrated stocks.

# Selection (Formation) Phase

The data a sample of 172 stocks and 138 ETFs traded on the NYSE and NASDAQ, with daily data from 2010 - 2019 provided by Stooq. In total, there are ~46000 possible pairings. Jansen uses some complex econometrics wizardry:

He looks at the drift, volatility and correlation **(pairwise metrics/heuristics)** of spreads to predict cointegration, then performs Engle-Granger and Johnassen cointegration tests to reduce significant pairs to those agreed by both tests (366 pairs).

Next, Jansen uses logistic regression to see if heuristics can predict cointegration (with the cointegration tests as true labels). Apparently, using heuristics can cut the universe by half.

# Trading Phase

He then uses a Kalman filter for a dynamic hedge ratio and Bollinger bands for the entry/exit thresholds. Anyway, the strategy had an average Sharpe of 0.75 and underperformed the S&P when backtested with Backtrader.
