Type: #atom
Atom: [[Option Fundamentals (N)]]
Topic: Quant 
Level: #Exploratory 

----
# Theoretical Value

**Theoretical value** is the proposition of a price one would be willing to pay now to break even in the long run. It is a **discounted expected value of IV at expiry** - an expected value of the intrinsic value the option will have at expiry.

# A General Option Valuation Framework

1. Discretize outcomes of underlying at expiry
2. Assign a probability to each of them or some probability distribution across the range of values.
3. Calculate the IV of option at that underlying price (e.g **from a payoff diagram**), then calculate expectation, and discount to present (depending on settlement).
4. Perform some trading action based on your valuation - if you value discounted IV at 90 and the spot ask (offer) is 60, you can lift the offer (opposite of hitting bids), exercise at expiry, and make some profit.

It's important to note probabilities of each outcome evolve over time - non-stationary.

# A Simplified Introduction to the Black-Scholes Model

Put-Call Parity Foreword- This is a statement saying there is a unique price relationship between (European) call and put, and the underlying (with the options have same expiry date and strike price). They are connected.

Riskless Hedging Foreword - B & S incorporated into their model a riskless hedge idea - there is a unique hedge ratio or position ratio between an option and the underlying s.t small price changes in underlying are offset exactly by the option.

The B.S model states at minimum we need to know: option exercise price & time remaining to expiration (fixed), current spot, interest rate over life of option, and volatility of underlying.