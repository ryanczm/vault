Type: #atom
Atom: [[Performance Measurements]]
Topic: Quant
Understanding: #Exploratory 

----
# Definition

The factor rank autocorrelation is the time series of the Spearman rank correlation of the alpha vector at time $t$ and $t-1$. It is a time series of a **lag-1 Spearman autocorrelation over time**. The idea is that if the f.r.a is low or even negative, the positions are constantly being **rebalanced over time very often**, incurring high **transaction costs and turnover**.

If two alpha factors have similar rank ICs, we choose the one with higher FRA. However, it's important to note that **factor rank autocorrelation has nothing to do with returns** - it's simply how much turnover or how much you go to market to transact to reshuffle your holdings.

If we only long/short a single instrument, then we can just use turnover - like a buy/sell signal plot like in R&K for iSentium's strategy.