Type: #atom
Atom: [[Interest Rates (Z)]]
Topic: Quant 
Status: #inprogress 
Level: #Exploratory 

----
# Zero (Spot) Rates

**The spot rate** is the YTM on a zero-coupon bond - the rate that prevails today for a time period corresponding to zero's maturity. E.g the 2Y spot is 6%.

# Short Rates

The **short rate** is the interest rate for that interval at different points in time. The spot rate is the **geometric average of short rates** for that time period due to **rollover principle**. Short rates can occur in the future (**future short rate**).

**Rollover Principle** - This refers to the idea that if a zero exists with a given yield and time to maturity, the short rates within this maturity period must geometrically average to that zero spot rate. Why? I don't know.

This principle is used to 'prove' why an upward sloping yield curve implies short term rates will rise: [example](https://ealdrich.github.io/Teaching/Econ133/LectureNotes/termStructure.html)and vice versa. However, this doesn't mean we can calculate future rates with certainty, this is a simplified model.

# Forward Rates

Forward rates are **future short rates** that occur in the **future** outside of the zero time interval. Above, our argument used a 3Y zero and future short rates from Y2 and Y3. However, a forward rate would refer to a rate beyond Y3 in this case.

Generalizing the rollover argument, the formula for a forward rate at year $n$ is $$1+f_n=\frac{(1+y_n)^n}{(1+y_{n-1})^{n-1}}$$ where $y_n$ is the zero rate for $n$ years.