Type: #atom
Atom: [[Individual Data E.gs (R)]]
Topic: Quant
Understanding: #Exploratory 

----
# Data Processing

**Real time sentiment signals (Daily Directional Indicator)** are produced by iSentium. They specialize in Twitter NLP. A **sentiment level is produced per minute** between 8.30AM and 4.30PM every day for the S&P. Sentiment for the **day** is aggregated using an EMWA over past 10 days.

# Strategy Overview

The universe is limited to 100 stocks most representative of S&P 500, filtered using **tweet volume** and **realized volatility**. The daily sentiment is used. 

Using sentiment scores of past two days, OLS is used to forecast the **S&P 500 forward return** for **an unspecified period** (?). Betas are evolved via a Kalman filter (incorporate historical information). The forecast is used as a long/short signal. If long, buy, if short, sell.

# Evaluation

Backtesting yields 13.7% annualized return since January 2013 to 2017, compared to 12.7% from S&P. R&K then show a buy/sell signal chart over time - **similar to factor rank autocorrelation** - to see transaction cost.

![[twitter_sentiment_strategy.png]]

Correlation is tested with other equity risk premia - 45% correlation with S&P but 5% correlation with Value, Momentum, Quality etc.

Ideally, a strategy uncorrelated with the market factor (S&P returns) is good because that neutralizes market risk. If the S&P is down, your strategy is still working fine (historically).


