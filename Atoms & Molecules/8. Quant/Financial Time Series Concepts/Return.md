Type: #subsubtopic
Atom: [[Financial Time Series Concepts]]
Topic: Quant 

----
Return over a holding period of time is measured by the percentage change in price from the start to the end of the holding period: $$R_t=\frac{R_{t+1}-R_t}{R_t}=\frac{R_{t+1}}{R_t}-1$$
* It is the ratio of the price at the end of the holding period divided by the price at the starting period and subtracting 1.
* Pandas provides the `df.pct_change(...)` method to calculate returns.