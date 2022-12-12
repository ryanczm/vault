Type: #atom
Atom: [[Portfolio Construction Models (N)]]
Topic: Quant
Understanding: #Exploratory 

----
There are four types of rule-based portfolio construction models - **equal position weighting**, **equal risk weighting**, **alpha-driven weighting** and **decision tree-weighting**.

## Equal-Position Weighting

**Equal position weighting** refers to allocating the same amount of capital to each instrument. E.g 4 stocks, 100k, then 25k per strategy - a buy signal means putting the entire 25k into that stock. The belief for this is that if a position is good enough to be in, no other info is needed about it.

## Equal Risk Weighting

**Equal risk weighting** refers to adjusting position sizes to risk so the least risky instrument has the highest alloaction, and the most volatile one has the least. This requires a risk measure that is comparable across instruments to get a ratio (e.g 2:1).

However, the issue is financial time series exhibit nonstationarity volatility (volatility clustering), so as volatility is a historical measure, it could change (Palomar).

## Alpha-Driven Weighting 

**Alpha-driven weighting** determines position size on the signal strength and historical performance of the strategy - the best historically performing strategies get the largest position size.
