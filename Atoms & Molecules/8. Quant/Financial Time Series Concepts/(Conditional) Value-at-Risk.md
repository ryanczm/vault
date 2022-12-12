Type: #atom 
Atom: [[Risk Measures]]
Topic: Quant 
Understanding: #Exploratory 

----
# VaR Definition

For a **given portfolio**, time horizon (e.g 5 days) and probability $p$, **value-at-risk** is informally the **maximum possible value of loss** during that **time horizon** for the **portfolio** for that **probability**. E.g a 1-day 95% VaR of $1m means there is a 5% probability within the next day the portfolio loses $1m.

# CVaR Definition

The **conditional value-at-risk** or **expected shortfall (tail loss)** is the expected loss conditioned if the loss is greater than value-at-risk.

# Methods of Calculation

Not sure if VaR period must **match** return period. E.g weekly VaR must be calculated from weekly returns. This implies VaR period must be > minimal return period (e.g 1 day VaR but only weekly return data, cannot calculate).

## Historical Method

Simply plot a histogram of historical returns and calculate the percentile cutoff of return. Then multiply return by the current portfolio value to get VaR. Then get the expected return value below that cutoff for CVaR. This assumes the for the **historical period** there were **no new positions taken (no buying or selling)**. 

## Analytical Method

Simply calculate the expected return for that period (e.g for 1-day VaR calculate average daily return) and standard deviation, then assuming a normal distribution, can find value of (C)VaR from the **quantile function (inverse c.d.f)** $\Phi^{-1}$. We have $$VaR_\alpha =\mu+\sigma\phi^{-1}(\alpha) \quad \quad \quad CVaR_\alpha=\mu + \sigma\frac{\phi(\Phi^{-1}(\alpha))}{1-\alpha}$$
## Monte Carlo Method

Using some **analytical prior model** to generate returns and volatility, simply run a simulation then apply the **historical method** or **analytical method**.

# Extreme Value Theory Application to (C)VaR

According to the **Fisher-Tippett-Gnedenko theorem (1943)** in **extreme value theory**, the **conditional tail distribution (c.d.f of a tail)**  can be modelled as a **generalized Pareto distribution**. To determine parameters of the distribution (model fitting), choose those that maximize the log-likelihood function of some portfolio return data.

Then, you have an analytical distribution and maximum-likelihood parameters that you can use the generate p.d.fs and c.d.fs and samples to calculate your CVaR from.
