Type: #atom
Atom: [[Random Walk, GBM & Wiener Process (W)]]
Topic: Quant 
Status: #inprogress   
Level: #Exploratory 

----
# Overview

Wilmott uses a coin-toss game to build intuition for properties of the WP/BM. Note, no drift term yet, so just BM, not GBM.

# The Markov Property

This means the value of the next step is dependent on only the previous step. Fair enough.

# The Martingale Property

This has to do with conditional expectation. If you cut off the process till a point, then the expected value of that process from then on is still where it is cut off. If you play a coin toss game where a tail means you lose 1 and a head means you gain 1, then your expected winnings after $n$ tosses is the amount you already hold.

# Quadratic Variation

The quadratic variation says that if you chop one big interval into smaller intervals, then you take the squared variation within each subinterval and add it together, it is equal to the total variation of the interval (WTF?!):$$\sum_j^i(S_i-S_{j-1})^2$$


