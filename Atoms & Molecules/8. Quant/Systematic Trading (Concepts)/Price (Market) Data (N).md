Type: #atom
Atom: [[Data (N)]]
Topic: Quant
Understanding: #Exploratory 

----
# Definition

**Price (market) data** refers to not just prices of instruments, but other information received or derived from exchanges or transactions. These are all the information generated directly from the exchanges.

# Market Data Varies for Asset Class

Different asset classes have different forms of market data. They are generally **time series**. E.g **equities/futures** data in terms of **price**, **bond data** in terms of **yields**, **option contracts** in terms of **option chains**, FX data in terms of **exchange rates**.

# Market Hours

There are **pre-market**, **market** (e.g 9.30am-4pm) and **postmarket hours**. These originated because the SEC mandates a **trading halt** for companies who make **material announcements** (any news relating to company business). Hence, companies are inclined to make these announcements outside of market hours. Then, exchanges introduced after market hours. Outside-market hours have lower volume and liquidity. Markets close **during weekends & holidays** - no trading at all. 

# Tick Data

**Tick data** (a tick is the minimum upward or downward movement in the price of a security). Tick data is the the data of the **stream of trades that have occurred on the exchange** (the tick data is not the order book!). Each element is a tick. A tick contains: 

* **Time of Event** - Each tick does not occur at uniform frequency! We have to bucket by time and by security.
* **Ticker Traded** 
* **Trade Data** - Price and volume of transaction
* **Quote Data** - Bid and ask size and price

# OHLC Data

An **OHLC (open, high, low, close)** chart is bucketed tick data. It shows individual OHLC bars per unit time (e.g day). Each bar has 4 points, the open, high, low, close. We can use OHLC to eyeball intraday volatility (by looking at the open and close)

# Volume Data

**Volume** - refers to the trading volume at an interval. In general, **increases in volumes correlate with price movements** (more people are buying or selling) - is there a situation where volume increases sharply but price does not move (more people are buying and selling)? 

**Short interest** - If an asset rising is being shorted, short sellers will cut losses buy closing their short by buying the stock at market price. Short interest is the number of shares sold short / number of outstanding shares. Then, we can have an **alpha factor of high price momentum conditioned on high short interest**.