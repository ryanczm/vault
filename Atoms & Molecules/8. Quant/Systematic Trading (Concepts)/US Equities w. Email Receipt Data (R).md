Type: #atom
Atom: [[Business Processes E.gs (R)]]
Topic: Quant
Understanding: #Exploratory 

----
# Data Preprocessing

Eagle Alpha provides transaction data of online purchases. The dataset of transactions was for 97 companies, 31 in S&P500. They have email receipt time series data, which has 3 series: `dollar spend`, `number of orders` and `number of buyers` for each company. 

They **aggregate (resample)** the daily time series into **weekly**, and calculate week-on-week percentage change (e.g weekly 'return'), then winsorized (5th-95th percentile).

Then, these were either ranked or z-scored with past 4/5/6 weeks percentage change as separate signals. They long the top 5 and short bottom 5, rebalanced weekly.

Performance was generally Sharpe ratio of <1.

![[email_receipts_strategy.png]]
