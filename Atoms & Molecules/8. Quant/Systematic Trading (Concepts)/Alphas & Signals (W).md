Type: #theorem
Atom: [[Alpha Model Specifications (N)]]
Topic: Quant
Understanding: #Exploratory 

----
## Alpha

Note an **alpha** is a subset of a signal. An alpha is an **expression/logic applied to data that outputs a vector of real numbers (alpha vectors) whose values are proportional to the size of the positions you will take of each asset**.

* Not to be confused the other meaning of **alpha** (excess returns over a benchmark).
* A **signal** is then an **alpha vector**.

## Signal

A signal, from a semi-deterministic perspective, is a time-indexed, integer/real-valued Boolean `ndarray` produced from a time-indexed price `ndarray` representing the **positions** we wish to take in a set of instruments.

In the most basic form, if it is a long signal, then `1` corresponds to buy while `0` corresponds to sell. In a short signal, `1` corresponds to borrow and sell, and `0` corresponds to buy. 

It can take on a value of `n`, which indicates the position size - number of instruments to buy or sell. It captures the series of decisions to be made - when, what, how, amount.

The signal is then 'applied' to a price/returns `ndarray` to evaluate the performance - equivalent to executing the series of decisions on historical data to get the return of the strategy, which returns another `returns ndarray` - the **return series of the strategy or portfolio**.