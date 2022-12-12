Type: #atom
Atom: [[Data Processing (W)]]
Topic: Quant
Understanding: #Exploratory 

----
## Rolling Window Statistics

A r.w.s is a alternate specification of a price series produced from recomputing each observation as a function of the past $n$ observations - incorporating price information of a recent history but in a non-Bayesian fashion (unlike Kalman filtering).

### Simple Moving Average (Rolling Mean)

The SMA is a type of rolling window statistic. It is the moving average of the past $n$ days computed across all $T-n$ days to form a **rolling mean time series**.

### Bollinger Bands

John Bollinger did some technical analysis in 1977. Bollinger bands are a r.w.s that is a **price envelope**. The rolling s.d and mean are calculated, then we add a scaled standard deviation to the s.m.a $\mu_i \pm k\sigma_i$ to get the upper and lower band values. 
