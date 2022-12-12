Type: #atom
Atom: [[Engineering Alpha Factors (J)]]
Topic: Quant 
Understanding: #Exploratory 

----
# Notebook Overview

In this notebook, Jansen takes Quandl equities data (2400 stocks from 2008-2018) and manually creates features/factors with pure  `pandas` wizardry, unlike in AI4T where `zipline` was used.

# Fama French Rolling Regression for Rolling Factor Betas

We read in Fama french data using `Pandas DataReader`, then join it to our monthly return data. Then, we group by ticker (producing a dataframe for each ticker). Then, we `apply` a `RollingOLS` to each ticker to estimate factor betas. Thus, each month's factor beta (exposure) is the slope from regression against the past 2 years (window length) of data.

# Factor List

The list of created factors is below:

```
Index(['return_1m', 'return_2m', 'return_3m', 'return_6m', 'return_9m', 'return_12m', 'Mkt-RF', 'SMB', 'HML', 'RMW', 'CMA', 'momentum_2', 'momentum_3', 'momentum_6', 'momentum_9', 'momentum_12', 'momentum_3_12', 'year', 'month', 'return_1m_t-1', 'return_1m_t-2', 'return_1m_t-3', 'return_1m_t-4', 'return_1m_t-5', 'return_1m_t-6', 'target_1m', 'target_2m', 'target_3m', 'target_6m', 'target_12m', 'age', 'msize', 'sector'], dtype='object')
```

