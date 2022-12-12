Type: #theorem
Atom: [[Time Series Definition (S.P)]]
Subtopic: Time Series
Topic: Statistics
Understanding: #Exploratory 

----
Weak stationarity is a property of a time series. A time series is weakly stationary if it is **mean stationary**, **variance stationary** and **covariance stationary**. It means the lower order moments (mean, variance, covariance) are **invariant to time shift** and higher order (>2) moments of the r.v change with time.

# Mean Stationary

Mean stationarity implies the expectation of the process is constant and is time-invariant - graphically, there is no trend at all.$$\mathbb{E}[X_t]=\mu\neq f(t) $$
# Variance Stationary

**Variance stationarity** is a condition for weak stationarity. It implies the variance $\sigma^2$ of the process is constant and time-invariant. Graphically, the **volatility is constant across time (no heteroskedasticity)**.
$$Var(X_t)=\sigma^2\neq f(t)$$

# Covariance Stationary 

**Covariance stationarity** implies the autocovariance is a function of lags and not time. This means the autocovariance is constant. Graphically, covariance stationarity is like **constant horizontal volatility** - the periodicity is somewhat constant over time.

$$Cov(X_t,X_{t+h})=f(h)\neq f(t)$$

