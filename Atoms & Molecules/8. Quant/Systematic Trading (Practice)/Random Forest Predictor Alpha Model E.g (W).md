Type: #atom
Atom: [[Strategy Projects (W)]]
Topic: Quant 
Understanding: #Exploratory 

----
# Alpha Model Overview

This alpha model is a cross-sectional equities alpha model that aims to use certain factors and features in a random forest to predict lookahead quantile returns. Alpha vector is emitted daily, weights change daily (TBC)? 

* Gaps in understanding in how to create alpha vector from model output.
* Sharpe on validation was 3.77 but on test was 1.21. 

# Factors & Features

Factors - The factors used are **Momentum 1Y**, **Mean Reversion 5D Sector Neutral Smoothed**, **Overnight Sentiment Smoothed (Overnight returns)**. The last factor is the **trailing 10-day moving average of nightly overnight returns**.

Features - The **individual asset features** are annualized 20D and 120D volatility and average dollar-volume, sectors (one-hot encoded). **Market-wide regime features** are 20D and 120D market volatility and average dispersion. **Date features** are the usual.

The tricky parts are implementing **overnight sentiment** and **market volatility and dispersion**, requiring inheriting from `CustomFactor` and building a custom class.

# Target

The target is the 1-week (5 working days) quantiled return.  We first create quantiled returns, then shift them forward. We plot rolling autocorrelation of increasing days of shifted returns against original to observe overlapping labels problem.

The tricky parts are working with Pandas `MultiIndex`.

# Train-Valid-Test Split

Use temporal splitting on our dataframe.

# Model

We train the model and plot accuracy as a function of number of trees. Interestingly, accuracy is only around `0.50-0.55`.

We try out non-overlapping samples, and 