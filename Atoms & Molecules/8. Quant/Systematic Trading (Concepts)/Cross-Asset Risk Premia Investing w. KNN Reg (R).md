Type: #atom
Atom: [[Regressions Strategies E.gs (R)]]
Topic: Quant
Understanding: #Exploratory 

----
# Strategy Overview

**KNN regression** is a **non-parametric method** (there are no model parameteres to be fit at all). It takes, given a dataset of feature vectors (points in vector space), and a sample vector (new point), find the K-nearest neighbour data points. Then, simply take the labels (can be a vector too!) and average them to get the prediction.

# Problem Setup

The idea is that they had cross-asset risk premia factors of Value, Momentum, Carry, and Volatility for equities, bonds, currencies and commodities. These are proven to deliver good Sharpe over a period of 40 years. The idea is that in different economic regimes, different style factors work better. 

They construct a monthly rebalancing strategy. They compute distance between economic regime vector (features) of current month to economic regime vector for all months in past 10 years (120 data points). Using KNN regression, find K-nearest neighbours. 

For each neighbour (nearest economic regime vector in the past), find average return of the succeeding month for all 20 cross-asset risk premia factors.

Each neighbouring economic regime vector month has 20 average returns of cross-asset risk premia factors. They average this out to form one vector of returns. They sort by highest returns,

Then they choose a subset $S$ that performed the best. Then, they rebalance the portfolio to get exposure to these $S$ factors.

For $K=2$ and $S$=8

