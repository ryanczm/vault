Type: #atom
Subsubtopic: [[Portfolio Optimization (W)]]
Topic: Quant 
Understanding: #Exploratory Intuition

----
# Definition

**PnL attribution (return decomposition)** refers to decomposing the portfolio PnL for one time period into the various risk factors.

# Return Decomposition

Portfolio PnL for one period is the holdings multiplied by each assets return. This can be decomposed using the risk factor model expression for return $$h^Tr= h^T(B^Tf+s)=h^TB^Tf+ h^Ts=\sum_i^ke_if_i+ h^Ts $$
Which decomposes return into **alpha and risk factors and idiosyncratic return**. But how do we include this inside? Wouldn't this mean $B$ and $F$ contain alpha factors as well. Then, wouldn't the alpha model need to be linear (e.g OLS and not RF).