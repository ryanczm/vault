Type: #atom
Atom: [[Paper Case Studies (W)]]
Topic: Quant 
Understanding: #Exploratory 

----
# Paper Overview

A paper titled **Overnight Returns and Firm-Specific Investor Sentiment by David Aboody** in 2015 posits two hypotheses:

1. Overnight returns (close-to-open returns) are **mean-reverting later in the afternoon**.
2. The **one-week average overnight return** is a momentum factor reflective of retail investor sentiment in the short term (several weeks?). 
3. Stocks with high positive overnight returns are mean-reverting in the long term (next 12 months).

# Implementation Overview

We need to create a custom factor class that inherits from `CustomFactor` class. We need to create the `CloseToOpenReturns` factor and `TrailingOvernightReturns` factor (weekly), then if the one-week average overnight return is high, we would long the stock???

# Underlying Behavior

Why would the weekly overnight returns mean anything in terms of future returns?