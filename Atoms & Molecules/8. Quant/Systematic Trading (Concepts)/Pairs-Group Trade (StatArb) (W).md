Type: #atom
Atom: [[Mean-Reversion Strategies (N)]]
Topic: Quant 
Understanding: #Exploratory 

----
# Definition

The idea for pairs-trading is to make a long and short decision once the spread between them hits a certain value. Hence, the spread is the signal that emits the decision.

# Hedge Ratios

The hedge ratio describes the amount of instrument B to purchase or sell for every unit of instrument A. E.g if the spread diverges too much from the mean and triggers a signal, how much do you long-short?

## Dynamic Hedge Ratio

However, somehow even if you historically identify cointegrated assets, we still need to determine a hedge ratio every time you trade. So you can do this dynamically via a Kalman filter.

# Pair Identification

Comparison is $\mathcal O (n^2)$, so not good. Simply cluster stocks prices time series together. But surely, this is not ordinary clustering - this is time series similarity/clustering!

# Long and Shorting the Spread

If the spread $A-B$ is significantly positive, we short the spread (short A and long B), if significantly negative, we long the spread (long A and short B).

To determine the significance of the deviation, we use the z-score of the spread based on the spreads historical mean.

# Generalizing Beyond Pairs to Groups as Stat Arb (!)

Pairs trading can be generalized to form a portfolio of similar stocks (a group) such that any spread between the individual stock and the portfolio of stocks is stationary. Then, simply perform the required positions when the spread deviates. 

* The group ($n$-asset) case is more tricky in terms of positioning. The Johansen test (check if $k$ series are integrated instead of a pair) is used. Jansen's ML4T shows an elementary example of this.