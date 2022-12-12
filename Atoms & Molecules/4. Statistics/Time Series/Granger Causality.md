Type: #atom 
Subsubtopic: [[Similarity]] 
Subtopic: Time Series
Topic: Statistics
Understanding: #Exploratory Intuition

----
# Overview

Granger Causality is a **hypothesis test** for determining whether **one time series is useful in forecasting another for a given number of lags**. It is done by building a b**ivariate autoregression model** : $$y_t=a_0+\alpha_1y_{t-1}+\alpha_2y_{t-2} + \cdots + a_my_{t-m} + b_px_{t-p}+\cdots b_qx_{t-q}+\epsilon_t$$ where we have **two sets of coefficients/parameters** to be estimated, $\alpha$ and $\beta$. And also the univariate autoregressive model for the target time series. Then, we simply take the statistic of the log of the variance ratio of errors, and if it is significant, we conclude using a bivariate model forecasts better than a single one, and $x$ *'Granger-causes'* $y$.

# Variance Ratio

$$GC=log(\frac{Var[e]}{Var[\epsilon]})$$
Where $e$ is the error series of the univariate AR model and $\epsilon$ is the series from the bivariate AR model.

# Stationarity Requirements

Do time series need to be stationary to perform a Granger Causality test? Yes, because it uses the AR family of models. Hence, **simply difference the series**.


---
Source: [Mike Cohen - Granger Causality](https://www.youtube.com/watch?v=XqsSB_vpHLs&ab_channel=MikeXCohen)
Clive Granger (1934-2004) argued that causality in economics could be tested by measuring the ability of a time series using prior values of another time series. He conceptualized it in a 1969 paper in *Econometrica*.