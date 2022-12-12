Type: #atom
Atom: [[Performance Measurements]]
Topic: Quant
Understanding: #Exploratory 

----
# Definition

The Sharpe ratio is a risk-adjusted return measure. It is the the ratio of reward to volatility. The numerator is the **risk premium (excess return/differential return)** and denominator is the **portfolio volatility or root of portfolio (sample) variance**. $$\frac{E[R_p-R_f]}{\sigma_p^*}$$
# Calculation

Calculate excess portfolio returns in each period, then calculate the expectation of this series (arithmetic or geometric). Then calculate the sample volatility/standard deviation from the series, and take the top divided by bottom. 

# Annualizing Sharpe Ratio

Annualizing Sharpe ratio is done in the same fashion of annualizing volatility - scaling by square root of ratio of periods.

# AI4T Usage

We calculated the Sharpe ratio of a preprocessed 1Y forward returns momentum alpha factor for a daily rebalanced portfolio.