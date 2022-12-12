Type: #atom
Atom: [[Regressions Strategies E.gs (R)]]
Topic: Quant
Understanding: #Exploratory 

----
# Strategy Overview

A simulated pairs trading straetgy between the MSCI Australia and MSCI Canada indices is used (no information how the pair was selected).

The hedge ratio was computed dynamically using a rolling linear regression and a Kalman filter, and a Kalman filter was shown to have slightly better Sharpe ratio: Since 2009, Kalman had 0.75 Sharpe and rolling regression had 0.68 Sharpe. Is this good? 

The hedge ratio is used to compute the spread. The spread is used to enter positions (using the ratio of the hedge ratio) based on some rule.