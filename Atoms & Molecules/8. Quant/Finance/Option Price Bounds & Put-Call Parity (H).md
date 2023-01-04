Type: #atom
Atom: [[Properties of Stock Options (H)]]
Topic: Quant 
Status: #inprogress   
Level: #Exploratory 

----
# Overview

These bounds are established by **no-arbitrage principle (good deal principle)**, which states that arbitraging a price difference (**buy low and sell high for instant riskless profit - take loan, buy low, sell high, repay loan**) is impossible - because of market forces.

# Upper Bounds on European, Non-Dividend Paying, Stock Options

**Calls** - For calls, the upper bound is the stock price - $c \leq S_t$ and $C \leq S_t$.  
Puts - The upper bound is the exercise. For American options, it is $p \leq Ke^{-rT}$ - the discounted exercise.

# Lower Bounds European, Non-Dividend Paying, Stock Options

**Calls** - It cannot be lower than the strike minus the discounted underlying: $c \geq S_t - Ke^{-rT}$. To see this, consider a portfolio $A$ of the call and a zero paying $K$ at $T$ (to exercise it), and a portfolio $B$ of one unit of the stock. The former is worth $\max(S_T,K)$ and the latter is $S_T$.

The argument is $c + Ke^{-rT} \geq S_t$. Otherwise, loan from bank to buy call and zero, exercise, sell underlying, repay bank, keep profit. 

**Puts** - This is just swapping the order of the call lower bound: $p \geq Ke^{-rT}-S_t$. Consider a portfolio $C$ of the put and the stock, and $D$ of the zero paying $K$ at $T$. Again, the former is worth $\max(S_T,K)$ and the latter is worth $K$.

# Put-Call Parity

Combining $A$ and $C$, we notice that when the underlying is greater than exercise, both portfolios are worth $S_T$ and $K$ when not. Thus, they will always be worth the same: $c + Ke^{-rT}= p+ S_0$ - 

To see this, consider where prices are s.t $A > C$. Then, we long a call, short the stock, short a put. We reinvest this money at risk-free rate. At expiry, we always end up buying the stock at $S_T$. We then use this to close out our short position. What remains is the profit.

See this [example](https://www.wallstreetmojo.com/put-call-parity/) (Wall Street Mojo).

# Bounds on American, Non-Dividend Paying Stock Options
