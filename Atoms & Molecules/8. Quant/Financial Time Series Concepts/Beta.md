Type: #atom
Atom: [[CAPM]]
Topic: Quant 
Understanding: #Exploratory Intuition

----
Beta is a measure of how an individual asset moves with the market. It is thus a measure of an asset's systematic risk. It is the slope of regressing the individual asset returns (target) on the market returns (independent variable): $$\beta_i=\frac{Cov(R_i,R_m)}{Var(R_m)} \quad \quad r_{i,t}=\alpha_i+\beta_i \space r_{m,t} + \epsilon_t$$
Beta being the ratio of covariance over variance only holds in the simple linear regression (univariate) case.  Beta can alternatively expressed as the correlation coefficient between the asset and the market scaled by the ratio of their volatilities: $$\beta_i=\rho_{i,m}\frac{\sigma_i}{\sigma_m}$$
This implies volatile instruments (same market vol) have higher beta but a more volatile market (same instrument vol) has lower beta.


### Beta Estimation Over Time

Market betas are not stationary (there could be jumps in the trend). Kalman filters can be used to estimate a Beta state over time based on some parameters.