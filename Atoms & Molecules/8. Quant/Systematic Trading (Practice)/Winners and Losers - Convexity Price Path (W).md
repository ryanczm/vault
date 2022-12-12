Type: #atom
Atom: [[Paper Case Studies (W)]]
Topic: Quant 
Understanding: #Exploratory 

----
# Paper Overview

A paper titled **The Formation Process of Winners and Losers in Momentum Investing by Chen, Wang and Yu** explain that stocks future expected returns can be partially explained by the path of the return - if it is convex or concave. 

Given two stocks with similar return over $n$ periods, the stock with higher return is the stock with a more convex shaped price path (accelerating) which can be modelled via $y = \beta t + \gamma t^2 + \alpha$.

We can model convexity via a **quadratic polynomial** with a **gain coefficient** and **acceleration coefficient** that quantify the movement. The ranks of `gain * acc` product becomes the Alpha factor - simply long if there is a high product and short if there is a low product.

# Implementation

We create a custom factor called `RegressionAgainstTime` that inherits from the `CustomFactor` class. This lets us create a `conditional_factor` which is the product of the gain and acceleration coefficient of the regression against time of the past year (252 days) datapoints.




