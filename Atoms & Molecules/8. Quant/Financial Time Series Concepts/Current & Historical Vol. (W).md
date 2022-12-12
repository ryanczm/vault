Type: #atom 
Atom: [[Volatility (Definition)]]
Topic: Quant 
Understanding: #Exploratory 

----
Volatility is just a **rolling window standard deviation of a log returns series**. **Current volatility** is the **current lagged volatility** (estimated using a lagged window of specified duration). It measures how much **differing perspectives (actions) & focus** are on a particular instrument. 

## Downsampling Volatility (Annualizing)

If you have monthly volatility (standard deviation of past month of daily log returns) and want to rescale this:
The scale factor on the r.h.s is the square root of the fraction to scale the r.h.s to the l.h.s - the longer the time period, the greater the volatility (remember standard deviation is sqrt of variance) $$\sigma_y=\sigma_m \space \sqrt{\frac{12}{1}} \quad\quad \sigma_m=\sigma_y \space \sqrt{\frac{1}{12}}$$
This represents resampling the historical time series to a lower or higher frequency interval.

## EMWA of Squared Log Returns

We can also estimate volatility by an exponentially weighted moving average of squared log returns **(assuming log returns have a mean of 0, we don't need to subtract from mean)**. In Pandas, once we have log returns, we just need to square each one, then pass an `emw` over with a `mean` function for a given $\alpha$.

## Market Volatility and Price Behavior

Since volatility is variability of returns, in a high volatility environment (**a regime**), we should expect many up and down price fluctuations, and thus **mean reversion strategies should perform better**. Conversely, in low volatility times, **momentum strategies may work better**.

The conventional idea is that in high-vol times (high VIX), prices go down, and in low-vol times, prices go up. But empirically, there were plenty of periods in S&P 500 history that contradict this empirically. So it's not always true.

