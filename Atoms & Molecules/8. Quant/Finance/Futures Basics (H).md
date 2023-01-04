Type: #atom
Atom: [[Futures & Forwards (H)]]
Topic: Quant 
Status: #inprogress 
Level: #Exploratory 

----
# Specification of a Futures Contract

We have the **asset**, the **contract size**, **delivery arrangements** and **delivery/expiry date**.

**Forwards vs Futures** - **Futures are standardized contracts settled daily traded on exchange**, a forward is simply a pure contract with no settling. Because of the mechanics, traders trade futures and farmers (or commodity sellers and consumers) use forards.

# Convergence of Futures to Spot Price

As the delivery period for a futures contract is approached, the futures contract price converges to the spot price. This is because market participants will arbitrage any difference (if a futures price due to expire tomorrow is much higher than the spot, people will end up buying spot and selling/shorting futures until the price goes down).

# Settlement (Variation)

From the transaction date (long party enters into a contract with a short), the two parties margin accounts are connected from the transaction price. If I buy at 1000, price goes to 800 the next day, 200 goes from my account to the short party's account. If price goes to 1200 the day after, 400 goes from short party's account to mine. This cash flow is called **variation**.

No cash changes hands upon agreement of the contract.

# Contango and Backwardation

A price forward curve says, starting from now (spot price), if I take delivery in 10 months time, what price do I pay?

Contango - The curve goes up - meaning it is more expensive to guarantee delivery in 10 months time.
Backwardation - The curve goes up - it is cheaper to guarantee delivery in 10 months time than today. Club tickets have a backwardated PFC curve - buying tickets in advance is always cheaper. Same goes for any event ticket.