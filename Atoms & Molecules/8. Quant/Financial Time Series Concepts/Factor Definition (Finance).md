Type: #keyatom
Subsubtopic: [[Factors]]
Topic: Quant 
Understanding: #Exploratory  Understanding

----
# Factor Definition

A factor is a **list of numerical values**, one for each stock, **potentially predictive** of an **aspect of performance** of these stocks in the **future** or a key driver of returns. **Factors** are used in a **factor model** to predict. They are similar to features in data science, but the **creation and choosing process** is much more complex.

# Factor Specifications

## Forecast Horizon

Factors can be **current-looking** or **forward-looking**. **Current-looking factors** predict the current price given current data and **must be forecasted** to predict future returns. **Forward-looking factors** predict future price in a window of $n$ days ahead given current data. This depends on the **time indices**, e.g $x_{t-n}$ regressed against $y_t$
makes a factor forward looking.

# Structure

Factors can be **single-stock/instrument** or **multi-stock/instrument (cross-sectional)**. For **cross-sectional factors**, **standardization** is required so their sum adds to 1. Factors can be cross sectional be simply using the same data $X$ on different instruments/stocks $y$. E.g the same data predicts returns for different stocks.

# Construction

Factors can be any time series, but often they are **returns** constructed from **hypothetical portfolios** of instruments that have **particular characteristics**.