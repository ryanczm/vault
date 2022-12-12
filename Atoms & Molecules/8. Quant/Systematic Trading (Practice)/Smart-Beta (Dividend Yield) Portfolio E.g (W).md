Type: #atom
Atom: [[Strategy Projects (W)]]
Topic: Quant 

----
# Strategy Overview

This is the note for the third strategy in AI4T - a Smart Beta portfolio focused on **harvesting dividend yield**. As mentioned, Smart Beta portfolios are passive, long-only, infrequently rebalanced portfolios based off modifying index weights to **balance** between **index tracking** and the **target factor exposure**.

The `index_weights` are computed from dollar-volume (turnover), and dividend exposure is calculated from historical `dividends` (DataFrame of dividend payouts over time for each stock) which gives trailing dividend yield.

# Signal Construction - Calculating Index Weights & Dividend Weights

The expression to calculate dividend weights
```Python
(np.cumsum(dividends)).div(np.cumsum(np.sum(dividends, axis=1)), axis=0) 
```
We divide the cumulative sum of dividends for each stock by the cumulative sum of total dividend payout for all stocks for each time period. So e.g if AAPL had cumulative dividends of $5 per share at the 30-day mark, and the total cumulative dividend payout for all companies in the portfolio was $500, then AAPl gets a 0.01 weight at that time period in our Smart Beta portfolio.

# Signal Execution - Calculate Weighted Returns

We can apply our weighting scheme (DataFrame of weights) to the return dataframe. After that, since by definition Smart Beta is long-only, we use compounding via `cumprod`

# Performance Evaluation

We calculate annualized tracking error, which is the scaled (annualized) standard deviation of absolute difference between the Smart Beta return and index return.






