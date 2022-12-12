Type: #atom
Atom: [[(Weak) Stationarity]]
Subtopic: Time Series
Topic: Statistics
Understanding: #Exploratory 

----
Differencing is a technique in time series which transforms the series into the differences between its consecutive observations where the differenced series only has $T-1$ values$$y'_t=y_t-y_{t-1}$$
* Differencing a random walk model $y_t = y_{t-1}+\epsilon_t$ leads to random noise.

# Higher Order Differencing

We can do higher order differencing - for example $2^{nd}$ order which we can compute by expanding out $$\begin{gathered}y''_t=y'_t-y'_{t-1} \\=(y_t-y_{t-1})-(y_{t-1}-y_{t-2})\\=y_t-2y_{t-1}+y_{t-2}\end{gathered}$$
# Seasonal Differencing

Seasonal differencing refers  to taking a seasonal ....


# Order of Integration

The order of integration is the minimum number of differences needed to obtain a [[(Weak) Stationarity|weakly stationary]] time series.  A time series is integrated of order $d$ if  $$(1-L)^dX_t$$
Where $L$ is the lag operator and $(1-L)$ is the first difference.

* To determine the o.o.i, simply run a stationarity test, difference if needed repeatedly until the test passes.

----
Source: [Wikipedia - Order of Integration](https://en.wikipedia.org/wiki/Order_of_integration)
