Type: #atom
Subsubtopic: [[Time-Series Risk Factor Models]]
Topic: Quant 
Understanding: #Exploratory  Understanding

----
# Definition

The **Fama-French model** is a risk factor model. It is the CAPM augmented with two additional factors - the **size factor (SMB)** and the **value factor (HML)**. This is the 3-factor model. The 5-factor model augments the 3-factor model to add **profitability (RMW)** and **investment (CMA)** factors. These are all derived from **financial statement data**, a form of **fundamental data**.

# Factor Generation via Theoretical Portfolios

The factors are generated from the returns of hypothetical portfolios of long (e.g small cap) and short (e.g large cap) stocks over time with equal weight in each stock, then calculate the daily or monthly return. Thus, the factors can be updated with current prices and increase in sample size over time.

Fama and French constructed the portfolios from factors from recursively making portfolios from size > value (e.g take the top quantile in size and sort by value) to restrict the total universe to those that fulfill size requirements.

# Size

The SMB factor comes from sorting stocks in an estimation universe via **market capitalization**.

# Value

The HML factor comes from sorting stocks in the e.u via **book-to-market ratio** (assets - liabilities / market cap) and doing the long-short equal weighted portfolio. Low b.m ratio companies are **growth**. High b.m ratio companies are **value**.