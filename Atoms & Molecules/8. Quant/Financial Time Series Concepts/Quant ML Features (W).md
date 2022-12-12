Type: #atom
Subsubtopic: [[Classical ML Alpha Models Setup]]
Topic: Quant 
Understanding: #Exploratory  Understanding

----
# Redefining Features

In alpha models using machine learning, the 'features' are alpha factors and features (eg. sector, year, quarter) which are not direct alpha factors but **interact with the alpha factors conditionally via the ML model**. Features do not specify a return mean/direction like an alpha factor.

# Universal Quant Features

These are canonical features that are often used in quant machine learning as **non-alpha factor features**.

## Instrument Specific Features - Instrument Volatility and Dollar Volume

These are **volatility** and **average dollar volume**. E.g high dollar-volume over a window of time may indicate some momentum factor is significant (if lots of people are buying and selling, prices go up empirically *brrr*). 

## Market Regimes - Dispersion

**Dispersion** is a summary statistic of a **cross-section** of instrument return - it is the deviation of the cross-section of returns. If the dispersion is low, then choosing the long/short of instruments doesn't capture alpha. If dispersion is high, then long/short is more effective. 

We can use a simple smoothed moving average of dispersion and volatility.

## Market Regimes - Volatility Regime Feature

A **market regime** is a **cluster of persistent market conditions** over a time period. A high volatility regime theoretically correlates with success in mean-reversion strategies, and low-vol regimes correlate with success in value companies or fundamental factors. 

To calculate, we take the mean of cross-sectional returns (equal-weight universe) of our instruments, then calculate volatility off that. We can do this for a short time period and long time period. If the short-term volatility > long-term volatility, we are in a high vol regime. So a feature could be $vol_s - vol_l$.

## Sector

The sector might be useful because different stocks in different sectors may have unique price movements that can be attributed to different weights of other features. If we put sector in the model, the model can potentially learn how different sectors use different features. They can be **one-hot encoded**.

## Date Parts

**Window dressing** refers to an action where a fund sells underperforming stocks and buys stocks that have done well recently nearing a financial reporting period (e.g end of quarter) for appearances' sake.

The **January effect** refers to funds selling poor stocks at the end of the year and buy them back at the start of the year to offset capital gains tax. 

Because of these kinds of seasonal and calendar effects, a machine learning model can use several date features: period variables (e.g `is_Tuesday`, `is_January`) and start-end features (`is_lastbusinessday`). These can be created with simple Boolean masking and `Pandas` `DateTime` functionality.