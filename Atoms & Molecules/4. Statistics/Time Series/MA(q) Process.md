Type: #atom 
Subsubtopic: [[Stationarity-Based (AR, MA)]] 
Subtopic: Time Series
Topic: Statistics

----
The moving average process is a common approach for modelling univariate time series. The process of order $n$ is given as follows with a constant $\mu$ term and an underlying white noise process (errors) $\epsilon \sim \mathcal{N}(0,\sigma^2)$ $$X_t=\mu+\epsilon_t+\sum_{i=1}^n \theta_i\epsilon_{t-1}$$
### Understanding the Error Term as a D.G.P

Ben Lambert assumes the error term (shocks) is a result of some latent strongly stationarity d.g.p that affects our observed variable.

* E.g predicting oil price $X_t$, then $\epsilon$ is positive if there is a typhoon and negative if there isn't and $\theta_i>0$. Then a typhoon shock propagates and increases the price of oil (reduces supply). But if $X_t$ was the supply, then $\theta_i$ would be $<0$.
* The order of the MA process will increase the time impact of underlying changes in the d.g.p.
* The parameters, $\theta$  somehow capture the impact of the d.g.p by finding the best parameters that fit the historical data, then can be used to forecast.


---
Source: [Ben Lambert Undergrad Econometrics - MA Processes](https://www.youtube.com/watch?v=uyIY8ddims0&list=PLwJRxp3blEvZyQBTTOMFRP_TDaSdly3gU&index=175&ab_channel=BenLambert)
Ben explain's how to derive the moments (mean, variance, autocovariance) of a $MA(1)$  process to prove the weak stationarity process.