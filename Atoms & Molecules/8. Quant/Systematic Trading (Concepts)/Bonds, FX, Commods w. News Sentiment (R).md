Type: #atom
Atom: [[Individual Data E.gs (R)]]
Topic: Quant
Understanding: #Exploratory 

----
# Data Preprocessing

Ravenpack provides a raw newsfeed in CSV form in terms of events (short text) Data from 2005-2017 was used (150GB of CSV files). They isolate all events specific to a country, currency or commodity via keywords. The data is of the form `event, relevance, event_sentiment_score`.

They filter by 'relevance' (Ravenpack provides a score for each event to be >75). They aggregate daily sentiment for a given entity for a daily signal.

# Strategy Overview

They use a daily long-short strategy of sovereign bonds from Australia, Canada, Denmark, Japan, etc etc. They  use the above sentiment indicator to long the 3 bonds with most negative sentiment, and short the 3 bonds with most positive sentiment (mean reversion). Rebalanced daily.

The signal was either the past day or a moving average lookback window. A 1M lookback produced 0.45 Sharpe ratio but 1D produced -0.10 Sharpe. 

This implies these sovereign bonds prices are negatively correlated with positive economic indicators for the past month - a negative economic indicator for the past month for that country implies bond prices will go up. No idea.

The same strategy was done with **equity indices** and **developed-market currencies**.