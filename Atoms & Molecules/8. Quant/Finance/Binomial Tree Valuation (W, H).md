Type: #atom
Atom: [[Binomial Model (W)]]
Topic: Quant 
Status: #inprogress   
Level: #Exploratory 

----
# Single-Step Tree Example

**Constructing a Riskless Portfolio -** We have a stock and a call on that stock expiring tomorrow. The stock is 100. It can go to 101 or 99 with $(p, 1-p)$. The $K=100$. If the stock goes to 101, the payoff is 1. If 99, the payoff is 1 (exercise). What is the option worth today?

It is $1/2$. To see this, we have a portfolio with 1 long call and $1/2$ short stock. If 101, payoff is 99/2 (option is exercised for a payoff of 1 and short $-0.5 \cdot 101$) . If 99, payoff is 99/2 (option is not exercised, short stock is $-99/2$).  Assuming interest rate is 0, portfolio is worth $-99/2$ today. Thus, if the stock is worth $-100$ today, the option must be worth $-1/2$.

**The Hedge Ratio** - We can do $1 - \Delta \cdot 101 = 0 - \Delta \cdot 99$ or $V_t = PV(V_{t+1})$ and solve for $\Delta=0.5$.

# Generalizing (Hull) - Deriving the Binomial Lattice Formula

We have initial price $S_0$, and at any time step, it goes to $S_0 u$ or $S_0 d$ where $u>1, d<1$. The payoff is $f_u | f_d$ in the up and down scenario. Now, we assume risklessness to get $\Delta S_0 u - f_u = \Delta S_0 - f_d$. So we have an expression for delta: $$\Delta = \frac{f_u - f_d}{S_0u - S_0d}$$
And now we can setup to price our option: the value of the portfolio today is the discounted value of the riskless portfolio at the next time step and solve for $f$, the option value. 

# Risk Neutral Valuation

Risk-neutrality means investors do not increase the expected return they require to compensate for increased risk. Risk-neutral valuation means valuing under this assumption. 

In a risk-free world, the future expected value of the stock is the current price, so we can find $(p,1-p)$, then somehow, this valuation applies to the real world too (proof?).


	