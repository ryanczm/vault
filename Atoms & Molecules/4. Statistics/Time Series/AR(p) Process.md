Type: #atom 
Subsubtopic: [[Stationarity-Based (AR, MA)]]
Subtopic: Time Series
Topic: Statistics

----
The autoregressive process specifies the output variable depends linearly on it's own previous values and on a stochastic term. Compared to the MA process, the AR is not always stationary. $$X_t=\epsilon_t+\sum_{i=1}^p \varphi_iX_{t-1}$$
Shocks propogate smoothly to infinity theoretically, but gradually decrease in impact. The shock is the underlying d.g.p, but the AR process captures the impact of shocks in a different way.


## Random Walks as AR(1) 

A random walk is a special case of an $AR(1)$ process with $\phi_1=1$. Writing the model out we get $$X_t=X_{t-1}+\epsilon_t$$ where $e_t$ is assumed to be a white noise process. Notice since $\sum \phi = 1$ is unity, the process is nonstationary.

## Innovation

Innovation is the difference between the observed value of $X_t$ and the optimal forecast conditioned on past values $[\hat{X_t}|X_{\tau\in t-1, \cdots,0}]$. 

* It is called innovation because it brings new ideas to the time series in an autoregression since new information from shocks will be captured in the next term recursively to infinity.

---
Source: [Ben Lambert Undergrad Econometrics - AR Processes](https://www.youtube.com/watch?v=AN0a58F6cxA&list=PLwJRxp3blEvZyQBTTOMFRP_TDaSdly3gU&index=176&ab_channel=BenLambert)