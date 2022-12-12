Type: #theorem 
Atom: [[Portfolio Fundamentals]]
Topic: Quant 
Understanding: #Basic Understanding

----
# Overview

Modern portfolio theory (mean-variance analysis) explains how an investor can make decisions to assemble a portfolio of assets to minimize variance for a given expected return: $$\min \frac{1}{2}w^T\Sigma w \quad \quad s.t \quad \quad m^Tw \geq \mu_b \quad \& \quad e^Tw=1$$
# Why Does Increasing Number of Assets (Diversification) Improve Sharpe?

The idea is that **adding uncorrelated assets decreases volatility (risk)**. To see this, portfolio variance is a function of the covariance matrix. There are $N$ variance terms but $N^2-N$ covariance terms. **Uncorrelated assets** means shrinking off-diagonal values to 0, reducing portfolio variance. 

Uncorrelated assets would ideally have, at a point in time, 0 return for asset A but high return for asset B, and so on, and this changes over time.

# Capital Allocation Line

The capital allocation line is expressed as the tangency line to the parabola of the highest Sharpe ratio portfolio on the efficient frontier (upper half of the bullet).

# Efficient Frontier

The **efficient frontier** is the locus of points $\{(\sigma_p,\mu_p)\}$ of optimal portfolios (highest reward for a certain level of risk) - the upper half of the **Markowitz bullet**. 

Given a universe and some historical data for a lookback period, we can randomly sample weights via some scheme (e.g Dirichlet distribution) and generate portfolios to plot on the risk-reward curve in Monte-Carlo style. We will notice the bullet/parabola shape forming after enough simulations.

----
Source: [Gregory Gundersen - Geometry of the Efficient Frontier](https://gregorygundersen.com/blog/2022/01/09/geometry-efficient-frontier/)
