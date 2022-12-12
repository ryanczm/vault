Type: #atom
Atom: [[Backtesting]]
Topic: Quant 
Understanding: #Basic Understanding

----
# Definition

**Backtesting** is a procedure how quants **simulate**, as **rigorously** as possible, what **would have happened** if a **trading strategy was deployed in production** **over a historical period** in order to **try and understand** how it might perform **in the future**.

# Validity

For a backtest to be considered valid, it must have a **realistic profit calculation** and **temporal realism**.

# Nitty Gritty Details

Backtesting and deployment requires one to be **very, very particular** about these details:

* Being Careful About **Units/Dimensional Analysis** - The units of your data, your factors, your holdings must all be specific and correct. E.g converting a factor in percentage to decimals, your transaction costs in terms of dollar amounts, etc.
* Being Careful About **Dates** - The dates must be correct. E.g shifting forward and backwards. 