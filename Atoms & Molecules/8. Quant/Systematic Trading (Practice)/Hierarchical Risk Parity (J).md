Type: #atom
Atom: [[Eigenportfolios & HRP (J)]]
Topic: Quant 
Understanding: #Exploratory 

----
# Overview

In this notebook, Jansen demonstrates **hierarchical risk parity** (invented by De Prado in 2016). It is a way, based off clever adaptation of hierarchical clustering, to assign portfolio weights.

# HRP Implementation

It is constructed from Scipy. Unfortunately, the default Scikit-Learn implementation is not tailored to MLDP's HRP, so it must be custom made to convert clustering ideas into proper weights.

# Strategy

From 2015-2017, on a universe of 1000 most liquid US stocks, Jansen uses the gradient boosting model to predict 1-day ahead forward daily returns. Each day, simply choose the top $n$ stocks with highest predicted returns (no weights!). Then, put these stock data into the HRP algorithm to compute weights. Rebalance daily.

No idea why this should even work anyway ...