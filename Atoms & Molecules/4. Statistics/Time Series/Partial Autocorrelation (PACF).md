Type: #atom 
Subsubtopic: [[Correlogram]]
Subtopic: Time Series
Topic: Statistics
Understanding: #Exploratory Intuition

----
# Definition

**Partial autocorrelation** (recursive residual autocorrelation) is derived from first calculating the lag plot of $r_1$ and fitting the line, then take the residuals and plot it against the next lagged time series and find the correlation, take the residuals and plot against the next lagged recursively.

# PACF and Removing Linear Dependence Between on Autocorrelations

PACF predicts the next lag from the residuals of the previous lag. The PACF of lag $k$, denoted $\phi_{k,k}$, is the autocorrelation between $z_t$ and $z_{t+k}$ with linear dependence on $z_t$ on $z_{t+1}$ through $z_{t+k-1}$ removed.

# PACF and AR(p) Parameters

Somehow, an AR(p) Process signature (ideal order) corresponds to a sharp PACF cutoff.