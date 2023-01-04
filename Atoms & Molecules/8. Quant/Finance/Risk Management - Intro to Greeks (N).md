Type: #atom
Atom: [[Option Fundamentals (N)]]
Topic: Quant 
Status: #inprogress
Level: #Exploratory 

----
# The Greeks

The *greeks*, or the *risk measures*, or the *partial derivatives*, let us analyze the effect of changing market conditions on option price/value.

These are **approximated empirically** from **market values** (how?) or some **model output** and are defined at a specific underlying/value for an option, e.g delta at underlying 40 (value 5)./

# The Delta $\Delta$ - $\frac{\partial V}{\partial S}$ (Slope/Directional Risk)

This is a measure of the option's value or V w.r.t the direction of underlying change (spot or S) - a rate of change of value with respect to underlying - the **slope**. Call deltas range from 0 to 1 and puts from 0 to -1. 

**Rate of Change -** The rate of change of option price can never be more than the underlying price change. Deep OTM, delta approaches 1, and deep ITM, delta approaches 0.
**Theoretical Position** - We can argue the delta is a theoretical equivalent to an underlying position
**Probability** - Another interpretation is that delta is the probability the option expires ITM.

# The Gamma $\Gamma=\frac{\partial \Delta}{\partial S}=\frac{\partial^2 V}{\partial S^2}$ (Curvature/Magnitude Risk)

The **gamma (curvature)** is the rate of change of delta with respect to the underlying - a second order greek.
If an option has a gamma of 5, for each rise in underlying point, the delta will drop or rise by 5. So if the option delta is 25, underlying move up by 1, delta goes to 30 (20).

We can use gamma to approximate an average delta over an underlying interval (as delta varies) Given underlying at 97.50, call with theoretical value of 3.65, $\Delta=40$ and $\Gamma=2.5$. So the delta at underlying 101.50 is 50. The average delta is 45. The new value is $3.65 + 0.45\cdot 4=5.45$.

# The Theta $\theta= \frac{\partial V}{\partial \tau}$ (Time Decay)

The theta is the rate of change of theoretical option value per unit time (e.g a day). Theta is usually negative with time, as time value decays.

# The Vega $\kappa$

The vega is the expressed change in theoretical value for 1 percentage point change in implied volatility. E.g vega of 0.15 implies the option gains (loses) 0.15 in value for each increase % in vol.

# The Rho $\rho$

The rho is the sensitivity of theoretical value 