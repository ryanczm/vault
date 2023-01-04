Type: #atom
Atom: [[Properties of Stock Options (H)]]
Topic: Quant 
Status: #inprogress   
Level: #Exploratory 

----
# Factors Affecting Option Prices

There are 6 factors affecting the price of a stock option: the underlying, the strike, time to expiration, volatility (realized and implied), risk-free interest rate, dividends. Note the risk-free rate discounts the PV paid (strike) exercising a call - making the underlying 'cheaper' and the call more valuable.

![[factors_affecting_option_price.png |500]]

# Upper Bounds

**Calls** - For calls, the upper bound is the stock price - $c \leq S_t$ and $C \leq S_t$.  
Puts - The upper bound is the exercise. For American options, it is $p \leq Ke^{-rT}$ - the discounted exercise.

# Lower Bounds

**Calls** - It cannot be lower than the strike minus the discounted underlying: $c \geq S_t - Ke^{-rT}$. To see this, consider a portfolio of the call and a zero paying $K$ at $T$, and a portfolio of one unit of the stock, then discount and rearrange. If this inequality wasn't true, you could buy the call and that zero and sell the stock for an arbitrage profit.
**Puts** - This is just swapping the order of the call lower bound: $p \geq Ke^{-rT}-S_t$.

