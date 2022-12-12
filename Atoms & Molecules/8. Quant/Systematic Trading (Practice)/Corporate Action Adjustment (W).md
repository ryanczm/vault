Type: #atom
Atom: [[Atoms & Molecules/8. Quant/Systematic Trading (Practice)/Data Processing (W)]]
Topic: Quant
Understanding: #Exploratory 

----
Corporate actions are a kind of fundamental data but impact price directly. These include **stock splits** and **dividends**. Prices must be **adjusted** to account for these corporate actions.

## Stock Splits

A stock split occurs when a company splits the stock, increasing the volume but decreasing price s.t market capitalization remains the same. This is to increase granularity and ensure better volume. A split causes a sharp spike decrease in price data.

**Adjusted price** is normalized price to smooth splits. We divide the price **before** each split by the split ratio (E.g 1/2 prices before a 2:1 split).

## Dividends

* **Declaration date** - Board announces intention to pay dividend
* **In-dividend date** - One day before ex-dividend. On this day, anyone who buys will be entitled, anyone who sells will not.
* **Ex-dividend date** - The day by which anyone who buys will not be paid. The expiry date.
* **Payment date** - Day which people get the dividend.

To normalize, we divide the price before the ex-dividend date by the **Adjusted Price Factor** $1 + D/S$
where $D$ is the dividend amount and $S$ is the price at ex-dividend. This is because we assume the price drops ex-dividend by $D$ the next day. Why? Presumably because dividend farmers sell it off