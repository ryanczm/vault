Type: #atom 
Subsubtopic: [[Similarity]]
Subtopic: Time Series
Topic: Statistics
Understanding: #Exploratory Intuition

----
**Cointegration** is a statistical property of multiple time series t If they are cointegrated, this (potentially) indicates some underlying true relationship between them that makes them move together. Formally, for nonstationary series $Y_t$ and $X_t$ of common order $d$, if their linear combination is weakly stationary meaning o.o.i of $0$,   $$\begin{gathered} \beta_1Y_t-\beta_2X_t=\epsilon_t\rightarrow I(0) \\\end{gathered}$$Then they are cointegrated. This implies their residuals $\epsilon_t$ follow a stationarity process. There are six possible tests for cointegrated series, but the **Engle-Granger Two-Step method** is most common. But there is another multiple cointegrated time series test, the **Johanssen test**.

## Engle-Granger Two Step Method

If we have two series we can simply regress one against the other to estimate the coefficient vector of best fit, then simply test (e.g via Dickey-Fuller) if the **residual series is stationary**: $$y_t=\beta x_t + \epsilon_t$$
# Correlation & Cointegration Relationship

![[cointegration_correlation.png]]

Consider **two series that move in tandem** except for a short period where one series bursts upwards while the other goes on as per normal. Then the series will show significant correlation, as the scatterplot will disregard the burst as outliers but there will be a good line of best fit - **but will not be cointegrated**. 