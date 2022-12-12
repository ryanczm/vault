Type: #atom
Subsubtopic: [[Transactions & Orders]]
Topic: Quant 
Understanding: #Exploratory Intuition

----
# Transaction Costs

Buying or selling produces price impact. Buying pushes the price upwards while selling pushes the price downwards. In large amounts. Transaction costs **reduce or chip away** at the returns from alpha factors, reducing the return.

# Limit Order Book

The **limit order book** is the **list of bids and asks** for an asset made by market participants. It is the **current market, at a given point in time, for the asset**. It is **limit** because the orders are **limit**. Market orders will take away the best bid and asks in the limit order book, leaving behind the remaining orders.  

# Parent and Child Orders

Often times, a parent order (e.g a **market order**) is broken up to smaller chunks of child orders at different quantities and prices.

# Transaction Cost Model

The trade size is the fraction of actual trade size divided by the ADV. The ADV measures on average, how much dollar volume was traded (changed hands) for an instrument. We can assume trade size is proportional to % change in price of instrument.

The idea is to **model transaction costs** for a trade and throw it into an objective function to '**minimize transaction costs**' by adjusting weights. 

There are linear and nonlinear transaction cost models. 

# How Transaction Cost Models in the Obj. Func Impact Trading

Apparently, a t.c.m in the o.f will impact the speed of position changes.