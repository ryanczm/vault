Type: #atom
Atom: [[Financial Economics Qns (C)]]
Topic: Quant 
Level: #Exploratory 

----
# Current Yield Curve Qn (TM capital)

Q: What is the current US yield curve?
A: [Gurufocus - Current US YC](https://www.gurufocus.com/yield_curve.php). Currently inverted (Dec 2022), 106bps spread (10Y-1Y). When we plot the spread, a negative spread historically is a leading indicator of economic recession.

# Implied Forward Rate Qn (3.3)

Q: The 5Y spot rate is 10% and 10Y spot rate is 15%. What is the per-annum implied forward rate from year 5 to 10? A: $[1.15^{10} / 1.10^{5}]^{1/5}-1=20.227\%$..

# Yield vs Rate of Return on a Bond Qn (3.4)

Q: What is the difference between yield on a bond and rate of return?
A: We have to answer with the assumptions of YTM - it is the RoR assuming the constant reinvestment rate of YTM and held to maturity. Whereas RoR is in practice - rates can vary after you buy the bond. E.g you buy a bond promising 5% coupon, but rates rise after you buy it. If you less the bond, you record a capital loss and negative RoR.

# Price vs YTM Convexity Qn (3.6)

Q: Draw the price vs YTM chart. Why is it convex? 
A: It is a mathematical artifact of how we discount bonds: discount a zero:  $C/(1+r)^T$. Nonlinear in $r$.

# Forward Pricing of a Bond and Zero-Coupon Bond Qn (3.9)

Q: Consider a 6M forward on a 10Y riskless discount zero. Is the forward premium or discount? If there are coupons > risk free rate, what happens?
A: $F(t,T)=S(t)e^{(r-\rho)(T-t)}$ - As the coupon rate is larger than the risk-free rate, this discounts the forward contract for the bond (backwardates it). Why? If not, people could long the bond, harvest the coupons (earning more than risk-free rate) and short a forward (guaranteed lift offer) in 6 months - arbitrage profit.

# Hedging a Bond Position with Bond Futures (3.13)

Q: You have a long position in a $100m 30Y bond. What can you do to limit your exposure to only $50m?
A: You should hedge by shorting the corresponding futures in the duration ratio (**your bond duration to the future duration**) multiplied by the number of contracts to match the position: $\frac{D_B}{D_F}\cdot k$;
