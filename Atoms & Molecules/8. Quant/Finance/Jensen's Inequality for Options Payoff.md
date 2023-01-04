Type: #atom
Atom: [[The Random Behavior of Assets (W)]]
Topic: Quant 
Level: #Exploratory 

----
# Overview

The stock price today is 100. In one year's time, it could be 50 or 150. How can we value an option on this stock with a strike of 100 expiring in a year?

The expected value is 100. Thus, we could say the option will be exactly at the money, and is worth 0. But this is wrong. Alternatively, we could look at payoffs then calculate expectation.

Let $f$ be the payoff function and $S$ be the stock price. Then $f(E[S])=0$ - the payoff of expected price is 0. But $E[f(S)]$ is 25 - if 50, payoff is 0, if 150, payoff is 50. Thus we have Jensen's inequality for a convex payoff function: $$E[f(S)]\geq f(E[S])$$ 


	