Type: #atom
Atom: [[Barra Optimization (W)]] 
Topic: Quant 
Understanding: #Exploratory 

----
# Building Tradelist Overview

After creating the code to optimize, we create `build_tradelist` and `convert_to_previous` functions and call the main loop:

```Python
trades, port = {}, {}
for dt in tqdm(my_dates, desc='Optimizing Portfolio', unit='day'):
    date = dt.strftime('%Y%m%d')

    result = form_optimal_portfolio(frames[date], previous_holdings, risk_aversion)
    trades[date] = build_tradelist(previous_holdings, result)
    port[date] = result
    previous_holdings = convert_to_previous(result)
```

This is to build the `tradelist`, a dictionary of `DataFrames` containing the optimal holdings and previous holdings for each period across all periods.

# Attribution

We can then examine the total PNL, the alpha PNL, risk PNL and cost PNL