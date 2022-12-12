Type: #atom
Atom: [[Cross Sectional Momentum Alpha Model E.g (W)]]
Topic: Quant 
Understanding: #Exploratory 

----
This denotes the second project in AI4T. It is a simple cross-sectional breakout momentum strategy on fake US equities data with a **group bet structure** that buys if a price exceeds the past high of $n$ days and shorts if a price drops below a past low.

# Strategy Overview (Breakout)

In this project, we implement a lame momentum strategy on a cross section of stocks (no pairs trade) via a breakout. If the **stock price exceeds the n-day lookback maximum**, long the stock (it's going up), if it **drops below the closing maximum**, short the stock (it's going down).

# Implementation

##  Alpha Logic - Calculating Lookback Highs and Lows

We use the `rolling` method to fill a DataFrame with the lagging 30 day high and lows. Then we compare it to the price dataframe to generate the signal.

## Signal Emission 

We compare the high-low dataframe to the price dataframe to generate the long and short signals respectively. We then do signal idempotency filtering for an arbitrary lookahead window. 

## Signal Execution

We then do the simple multiplication. However note the do-nothing signal, `0`, when multiplied makes the return for that period `0` as well. Somehow, log returns makes this work.

