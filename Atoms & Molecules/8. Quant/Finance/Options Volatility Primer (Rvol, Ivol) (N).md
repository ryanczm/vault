Type: #atom
Atom: [[Option Fundamentals (N)]]
Topic: Quant 
Status: #incomplete  
Level: #Exploratory 

----
# Lognormal Distributions

When percent price changes are normally distributed (returns), then continuous compounding of these price changes will result in a **lognormal distribution of price**.

To see this, scaling down reduces the proportion of downscaling whereas scaling up increases the proportion of upscaling.

# Timescale

If our contract is trading at 100 with a vol of 20%, what is the price change of 1 s.d daily? Well, we scale down the annualized vol to daily by dividing by 16 (root of 256) to get 1.14% x 100 = 1.25. Assuming normality, 66% chance of a movement $\pm \$1.25$ daily.

# Realized and Implied Volatility

**Realized Vol** - Realized volatility is the annualized s.d of percent price changes. For example, 52-week volatility refers to calculating weekly price changes over 52 data points, vs 50-day volatility (window and interval).

**Implied Vol** - This is the volatility implied from an option model when we tweak the vol parameter to move the initial theoretical valuation to the market valuation (current option price). This is then used by traders to compare relative pricing of options.

**Example** - For the same underlying, consider a 105 call offered at 3.60 with ivol of 28.50% and a 100 call offered at 5.40. While the 100 call is more expensive, it is cheaper in ivol (27.51%) by 99 bps. Traders use the ivol as the price (similar to yield).

Future realized volatility is the true future value while implied volatility is the 'forecasted volatility'.

# Impact of Vol on Price - Some Heuristics

1. A change in vol has a greater effect, in relative percentage terms on OTM options than ITM or ATM.
2. A change in vol has a greater effect on long-term option than an equivalent short-term option.
