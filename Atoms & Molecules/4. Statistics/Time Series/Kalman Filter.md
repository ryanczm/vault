Type: #atom
Subsubtopic: [[Continuous State-Space Models]]
Topic: Statistics
Status: #incomplete 
Understanding: #Exploratory 

----
# Overview (Intuition)

The Kalman filter requires quite complex matrix algebra formulas, so I will not attempt to understand the derivation of the algorithm or equations here. Rather, I will just develop intuition.

In finance, the Kalman filter can be used to dynamically estimate a model parameter, given new data, and update it over time. This can be used to **evolve/update regression betas over time** or replace **moving averages**.

# Finance Use Cases

## Kalman Filter to Evolve Betas

Kalman filters can replace a rolling window linear regression.
