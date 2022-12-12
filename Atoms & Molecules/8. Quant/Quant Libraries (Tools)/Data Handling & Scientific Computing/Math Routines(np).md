Type: #atom
Atom: [[Math-Based Routines (np)]]
Topic: Quant
Understanding: #Exploratory 

----
# Overview

There are quite a few categories of math functions. Some are element-wise, some are aggregation-based.

# Rounding

Round - `np.round()`, Floor - `np.floor()`, Ceiling - `np.ceiling()`. The 

# Sums, Products, Differences

These all require the `axis` argument. We have `np.prod(a), np.sum(a), np.nanprod(a), np.nansum(a), np.cumsum(a), np.cumprod(a)`, etc. The `nan` treats `NaN's` as a 1.

# Exponents & Logs

We have the usual `np.exp(a)`, `np.log(a)`, we can specify bases and the like.

# Arithmetic (Binary Operations)

These correspond to binary operations in `Pandas`. The signature is akin to `np.add(a1, a2, ...)`. These do not require an axis input because of **broadcasting**. We have `add`, `multiply`, `divide`, `power`, `subtract`, `fmod`, and lots more.

# Extrema Finding

We have a variety. Note `argmax/min` are in sorting, not math. We have `maximum(x1, x2)`, `minimum(x1,x2)`, etc. Note these take into arrays and compute, element wise, some extrema (compare between arrays).

# Miscellaneous

The useful ones are `np.sign(x)`, which returns the sign (-1 or 1) element wise, `np.absolute(x)`, and the nice winsorizing function `np.clip(a, a_min, a_max)`. We can do `np.clip(a, np.percentile(a, 0.05), np.percentile(a,0.95))` to do **winsorization**.



