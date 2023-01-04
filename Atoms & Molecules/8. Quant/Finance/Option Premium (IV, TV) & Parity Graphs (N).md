Type: #atom
Atom: [[Option Fundamentals (N)]]
Topic: Quant 
Level: #Exploratory 

----
# Premium, IV and TV, Moneyness

An option premium refers to the price of the actual option contract. The premium consists of **intrinsic value** and **time value**. We can decompose the premium because if we buy the option, we can always exercise it and gain the IV - it is always there. An option which is trading at IV is said to be at **parity** (0 TV). 

**Intrinsic Value** - IV is the difference between the exercise and current underlying price. For a call, it is $\max(0,S-X)$ and for a put, it is $\max(0, X-S)$. IV/moneyness is a credit to the long and debit to the short.

**Time Value (Extrinsic Value)** - This is the additional amount beyond a the IV that buyers are willing to pay for an option. If currently, the option premium is 50 and IV is 35, the time value is 15. This captures the aggregate 'hope' or 'probability' or 'belief' from speculators that the underlying will move in more favorable position to increase the value.

**Moneyness** - An option with +ve IV is in-the-money. An option wtih -ve IV is out-the-money. An option with 0 IV is at-the-money. 

**Automatic Exercise** - If an option is in-the-money at expiration, it will be automatically exercised so the holder (long) benefits.

# Parity Graphs/Hockey Sticks

A parity graph shows IV graphically. The **x-axis is (underlying) price with reference to strike**. The center is the exercise/strike price (fixed). To the left and right are lower underlying and higher underlying respectively. The **y-axis is IV**. It shows how IV changes as  underlying moves relative to strike.

**Combining Positions** - We can take multiple positions and overlay hockey sticks onto one graph. Increasing positions of the same type of contract increases the **slope steepness** (e.g you long 2 calls, then a +ve underlying will double your rate of IV increase).

To combine, we list out the contracts and positions in a table (contract on row, interval on columns) then calculate aggregate slope for each piecewise interval.

# Incorporating PnL into Hockey Sticks

Any long option position shifts the graph downwards (cost incurred), any short option position shifts the graph upwards. This shifts the breakeven point leftwards or rightwards (normally breakeven is at expiry). Shifting doesn't change slope.

# Using Parity Graphs

By constructing parity graphs, we can see how our underlying PnL changes or moves with the underlying for any complex position.