Type: #atom
Atom: [[Data Processing (W)]]
Topic: Quant
Understanding: #Exploratory 

----
We often think of stock prices as a continuous time series. However, it is discrete and often has missing values due to certain reasons.

### Weekends and Holidays

In a daily time series of stock prices, **weekends** and **holidays** will show a constant price because trading is closed then.

### IPOs & Delistings

Prior to an **IPO**, there will be no price data. This can be an issue if you are comparing multiple stocks time series and the observations are not injective. **Delisting** (private buyout or bankruptcy) also results in missing data.