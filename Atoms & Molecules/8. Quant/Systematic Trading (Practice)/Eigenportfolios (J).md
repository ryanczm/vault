Type: #atom
Atom: [[Eigenportfolios & HRP (J)]]
Topic: Quant 
Understanding: #Exploratory 

----
# Overview

In this notebook, Jansen demonstrates the Eigenportfolio technique. Essentially, one performs PCA on a covariance matrix of returns of stocks, and each principal component vector corresponds to the weights of one portfolio.

Eigenportfolios and it's application to pairs trading came from a paper by Avellanada in 2010 (*Statistical arbitrage in the US equities market*).

# Connection to Risk Factors

Apparently, eigenportfolios can be interpreted as risk factors.

# Eigenportfolios as a Rebalancing Strategy

One possible strategy is to do monthly rebalancing based on the eigenportfolio of a lagged window of returns. But why would this work anyway? The first eigenportfolio (first p.c) has very similar returns to the market. This is due to Klein's theorem (?).

# Relation to Pairs Trading

This [video](https://www.youtube.com/watch?v=IVAmm34eKWQ&ab_channel=Hudson%26Thames) by Hudson & Thames explains how pairs trading is done via Eigenportfolios. The underlying logic & derivation is quite complex, involving something called an S-score and some Brownian motion based model for price.

The idea is to compute eigenportfolios, then compute an S-score for each asset (a time series), which is analogous to the spread. Then, once the spread is far away enough, simply open a position on that asset and open opposite positions of the $\beta$ values of the eigenportfolio's exposure (remember each eigenportfolio is a risk factor, and we can do risk factor decomposition).