Type: #atom
Atom: [[Computations & Stats (pd)]]
Topic: Quant 
Understanding: #Exploratory 

----
# Overview

Most of these methods require an axis to compute along. `0` computes across a column, `1` computes across a row.

## Non-Axis Specific, Non-Aggregation

These include `.corr`, `.cov`, etc etc.

## Aggregation

These include `.max`, `min`, `.median`, `.std`, `.var`, `.prod`, `.cumsum`, `.cumprod`, etc. These are summary statistics.

## Non-Aggregation

These include `.rank`, `.round`, `.clip`, `pct_change`, etc. 

The `.quantile` function will return values at the given quantile across the specified axis. To compute quantile ranks as per return quantile, use `pd.qcut()` instead, which takes in a `Series` and the number of quantiles to return the quantile ranks.