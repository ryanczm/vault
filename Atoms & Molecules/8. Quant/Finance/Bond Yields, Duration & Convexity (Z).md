Type: #atom
Atom: [[Interest Rates (Z)]]
Topic: Quant 
Status: #inprogress 
Level: #Exploratory 

----
# Yield to Maturity

**Definition** - The YTM of a bond is the **annual yield that an investor would gain holding the bond to maturity for remaining $n$ periods assuming coupon reinvestment is the same rate as YTM**. 

**Illustration** - An example, given a market price of a 30-year bond selling at $1276.76 with 8% coupon rate paying semiannually would give a YTM of $0.03$ or $3\%$ per year. $$$1276.76=\sum_{t=0.5}^{30}\frac{40}{e^{rt}}+\frac{1000}{e^{30r}}$$ 

**Reinvestment Assumption** - This assumes the investor reinvests his coupon payments at the same return as the YTM. Why? Because each coupon is discounted using the YTM rate.

# Price and Yield as a Function of Years to Maturity.

The relationship looks something like this: it always converges to par as the maturity date nears.

![[bond_price_over_time.png|300]]

# MacAulay

The bond (MacAulay) **duration is a quantity (time) that is the expected period of the bond**, where **expectation weights** for each period are the proportion of present value of that cash flow for that time period. 

We calculate the weights for each period by calculating the PV of that cash flow, then dividing it by total PV (or calculate proportion of cash flow, then discount it) We then perform expectation on the periods using the weights for each period.

# Modified Duration

MD is the name given to price sensitivity and is the percentage change in price for a unit change in yield. Somehow, if a bond has MD of $k$, then a fall in interest rates in $1\%$ results in the bond price increasing by $k/100$.

A high duration bond means the expected time of cash flows is very far. So, a rise in rates would mean the high duration bond is a subpar or less attractive investment for a long period of time > steep drop in price.

# Convexity

Duration serves as a linear approximation. However, we can add a convexity (second derivative) term to make the approximation more accurate. The formula to then use both duration and convexity is a result of a Taylor series expansion. For the detailed formulae and derivation, see Crack's answer to 3.11.

**Negative vs Positive Convexity** - Positive is a normal convex curve (lower left quadrant). Negative is upper right quadrant.