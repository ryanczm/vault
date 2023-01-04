Type: #atom
Atom: [[Futures & Forwards (H)]]
Topic: Quant 
Level: #Exploratory 

----
# General Equation for Fair Value of a Forward Contract

What is the fair value of a forward contract? This is the determined by the cost and benefit of buying now compared to buying at some future date., and **assumes the spot price will be the same on delivery date**. $$F= S + C - B$$
**Costs and benefits** - These are the costs (e.g interest repayments for a loan) and benefits (e.g coupon payments or dividends or oil revenue from an oil well on the land) from owning the asset until the forward expiry date (e.g 1 year). Why? If you buy the forward instead of now, you are letting the counterparty absorb costs until you buy it off him - and he wants to be compensated.

# Fair Value in Continuous Time

The above equation is discrete. We can simply compound the costs and discount the benefits (see qn 3.9 in Crack): $$F(t,T)=S(t)e^{(r-\rho)(T-t)}$$
In this equation we compound the interest forgone and discount the coupon $\rho$.

The **basis** is the difference between $S$ and $F$, if forward price is higher then basis is negative (contango).

# Physical Commodities

$$F = C \cdot (1+r \cdot t) + (s\cdot t)+(i \cdot t)$$
Where $r$ is the interest rate (opportunity cost), $s$ is storage cost and $i$ is insurance cost. At first, basis seems always negative, but if a company wishes to obtain a commodity right now crucial to operations, this is called **convenience yield**. 

The convenience yield is the basis when it is positive (backwardation).

# Stock

# Bonds and Notes

# Currencies

# Stock and Futures Options