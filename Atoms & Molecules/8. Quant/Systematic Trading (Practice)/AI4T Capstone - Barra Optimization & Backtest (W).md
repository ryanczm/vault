Type: #atom
Atom: [[Strategy Projects (W)]]
Topic: Quant 
Understanding: #Exploratory 

----
# Strategy Overview

This is the **final capstone project** of AI4T. In this project, we use **Barra factor data** to create **alpha** and **risk factors**. Then, we build an **alpha model**, a **risk model**, a **transaction cost model** and put it into a **portfolio optimization model**. 

We build the **tradelist over time**, and calculate a **backtest** of the strategy. We also **decompose** the PnL via **attribution** and calculate **portfolio characteristics**.

# Barra Data

The Barra data contains **factor exposure data** for a universe of stocks identified by a **Barra ID**. We have 6 years of such daily data (252) from 2003 to 2008. There are 92 factors in total (**alpha and risk factors**). Factor exposures, not returns, because some factors are cross-sectional (e.g factor value is unit or null). 

We have 3 sources, `data` (factor exposure), `covariance` (factor covariances), and `daily_returns` (daily returns for the stocks in the universe). `data` and `daily_returns` are daily.

# Types of Factors

## Style Factors

Style factors are usually time series, non-categorical factors. Examples include beta, dividend yield, downside risk, earnings quality, earnings yield, growth, leverage, liquidity, momentum, profitability, value, management quality.

For example, **management quality** consists of asset growth, capex growth and capex. Asset growth is a regression of assets against time for the past 5 fiscal years. The slope is divided by average annual assets.

## Industry Factors

These are exposures to different industries, calculated via cross-sectional regression

# Data Preparation

The data is in `frames` for each day. We need to get our factor returns from regression.
