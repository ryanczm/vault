Type: #atom
Atom: [[Strategy Projects (W)]]
Topic: Quant 
Understanding: #Exploratory 

----
# Strategy Overview

In this exercise, we are tasked with coming up with a **dollar-neutral, zero-leverage portfolio optimization across ~490 stocks with an alpha and risk model**. We are supposed to evaluate the various factors using performance metrics (e.g rank IC, FRA, quantile analysis).

It uses 5 alpha factors: `MR 5D`, `MR 5D Sm`, `M 1YR`, `Overnight_sentiment`, `Overnight_sentiment Sm` which are arithmetically averaged (blended) into a single alpha vector that evolves across time daily. 

It uses PCA for the risk factor model, taking the first 20 principal components as risk factors. We incorporate the taught constraints - leverage, dollar-neutral, position, portfolio variance, and factor exposure constraints.

The only question is - how often does one run the optimization? Daily? Weekly? 
