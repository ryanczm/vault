Type: #atom
Atom: [[Types of Alpha Models (N)]]
Topic: Quant
Understanding: #Exploratory 

----
# Process

In a theory or hypothesis-based alpha model, one starts with a hypothesis. Then, from the **data**, we have the **universe definition**, **alpha discovery**, **alpha combination**, and **portfolio construction**.

## Price-Based Alpha Models

Price driven alpha models make use of **pure price data** to produce **decisions**.

**Trend models** are based on the investor perspective that **prices will follow a significant move in one direction** to form a trend. E.g the **MAC (moving average crossover)** method - given a financial time series an instrument, calculate a long period MA and short period MA series. When the MAs crossover, check their values. If the short MA is below the long MA for an arbitrary time period after the crossover, **short the instrument**. 

* A trend-following strategy on the S&P 500 index from Oct '07 to Nov '08 would have shorted the S&P after a crossover for the entire year.

**Mean reversion models** are based on the perspective that there is a **center of gravity around which prices oscillate (like a harmonic oscillator)**. This means the time series must be **mean stationary**. An example is the spread of SCHW vs MER from Jan '04 to Nov '06 - which exhibited mean reverting behavior. If the spread deviates statistically from the mean, simply long and short the respective instruments then reverse the positions once the spread hits the mean.

## Fundamental 

Fundamental driven alpha models make use of **macroeconomic and accounting data** to produce **decisions**.

**Value strategies** use fundamental metrics related to **firm value**. **Quant Long Short (QLS)** ranks equities by some fundamental metric (e.g Book-to-Price) ratio, then longs the highest ones while shorting the lowest ones.

**Growth strategies** use analyst growth metrics on companies to make decisions.

**Quality strategies** are either leverage, diversity of revenue sources, management quality, fraud risk or sentiment.
