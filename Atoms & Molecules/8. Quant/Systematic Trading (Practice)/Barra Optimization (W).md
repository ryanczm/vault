Type: #atom
Atom: [[AI4T Capstone - Barra Optimization & Backtest (W)]]
Topic: Quant 
Understanding: #Exploratory 

----
# Overview

The idea is to feed in data into the optimizer each day to get the weights. At each day, we need an input `DataFrame` containing:

* Alpha/risk factors - These are created from Barra.
* The data date (2 days prior)
* The return date (current day) and return (for backtesting)
* Previous holdings

We create the function `form_optimal_portfolio` which incorporates all the previous functions made. This takes in the `df` of data needed for that day, the `previous` holdings and `risk_aversion` parameter.
