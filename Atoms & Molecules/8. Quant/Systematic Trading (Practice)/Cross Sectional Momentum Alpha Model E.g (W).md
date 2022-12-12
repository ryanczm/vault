Type: #atom
Atom: [[Strategy Projects (W)]]
Topic: Quant 

----
This note overviews the first actual strategy project in the AI4T course, a simple cross-sectional momentum strategy on US equities data. It has monthly run frequency. It is used simplistically (equal dollar allocation) and implemented via simple `pandas` and `numpy` to produce signals and do a simple backtest.

# Strategy Overview - Cross Sectional Momentum

In this example, the idea is to take a universe of stocks, and apply a momentum based strategy to rebalance stocks every month end. Simply find the top and bottom $n$ stocks in terms of **monthly log returns**, then long the top and short the bottom with **equally weighted allocation**. 

Repeat this every month, and evaluate the portfolio returns over some period.

# Implementation

## Alpha Logic - Generate Forecasts: Getting Top/Bottom N for Each Month

## Signal Emission - Compare Forecasts to Prices

For each row in the stock dataframe, simply iterate, get the top n (flip sign for short), then do row assignment. 
```Python
 for i, row in prev_returns.iterrows():
        top_stocks.loc[i] = row.nlargest(top_n)
```
Then, use `~np.isnan(..).astype(int)` to convert to integer-valued Boolean dataframe. Do this for `short` and `long` signals. 

In this case, we are buying and selling equal dollar amounts of the stock (for simplicity) at each round.

## Signal Execution

Then, evaluate performance by multiplying the combined signal dataframe with the lookahead returns dataframe. Then, since the dollar allocation was split evenly, at each time period, simply sum `portfolio_returns.T.sum()` up the individual stock returns. This gives us a time series of portfolio returns (logged).

## Evaluate Performance (Backtesting)

Then, take arithmetic mean `.mean()` of portfolio log returns (monthly average log return), then annualize `*12` and convert to raw returns by taking the exponent of natural log.

---
[Github - Yuki678 - Project 1](https://github.com/yuki678/ai-for-trading/blob/master/module1/project1/home/project_1_starter.ipynb)
