Type: #atom
Atom: [[Time Series Models - Forecasting & StatArb (J)]]
Topic: Quant 
Understanding: #Exploratory 

----
# Overview

In this notebook, Jansen uses a VAR model to forecast consumer sentiment and industrial production. These are created by FRED - the Federal Reserve Economic Database, which the US government maintains. 

**Consumer sentiment** comes from monthly household survey census data from University of Michigan. For more information, see [Investopedia - Consumer Sentiment](https://www.investopedia.com/terms/c/consumer-sentiment.asp).

**Industrial production** measures levels of production and capacity in the manufacturing, mining, electric, and gas industries, relative to a base year.

However, Jansen differences the logged data, then forecasts the stationary series.