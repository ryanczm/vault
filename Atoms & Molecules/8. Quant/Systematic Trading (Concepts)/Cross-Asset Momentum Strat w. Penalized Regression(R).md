Type: #atom
Atom: [[Regressions Strategies E.gs (R)]]
Topic: Quant
Understanding: #Exploratory 

----
# Strategy Overview

The aim was to predict the 1-day forward return of several assets - S&P500, 7-10Y Treasury Bond index, US Dollar (DXY) and Gold. A 7-10Y treasury bond index is the average price of some bonds.  

They used 1M, 3M, 6M and 12M returns of these 4 assets, yielding **16 variables in total**, then used these 16 in a Lasso regression to predict the forward returns of each of the 4 assets. If positive, long, if negative, short.

The time period was 2007-2015. Each momentum strategy outperformed a long only position in the asset. But at what cost?

They also plotted evolution of betas (weights of feature as a function of the varying regularization parameter)
