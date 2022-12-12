Type: #atom
Atom: [[Price-Based Factors]]
Topic: Quant 
Understanding: #Exploratory  Understanding

----
# Overview

Technical-based factors are a type of price-based factor. Examples include RSI, BB, MACD, etc.

# RSI (Relative Strength Index)

RSI is a value between 0 and 100. RSI is usually used as a mean-reversion (reversal) factor, where we short it at a high value (e.g 70) and long at a low value (e.g 30). The formula uses average gains and average losses over a lookback window. 

E.g if lookback is 14 days, calculate the average closing return (if positive, gain, if negative, loss) over the past 14 days, then put it as a ratio and into the formula. 

# MACD (Moving Average Convergence/Divergence)

MACD is the short term EMWA (exponential) minus long term EMWA. If it is positive, this indicates momentum (shorter moving average > longer moving average).

# Bollinger Bands

Bollinger bands are upper and lower 'bands' computed by multiplying standard deviation of a windowed historical moving average. Obviously, the more volatile the recent window, the higher the bands.

