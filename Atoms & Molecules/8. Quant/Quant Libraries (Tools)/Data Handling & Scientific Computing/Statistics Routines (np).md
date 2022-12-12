Type: #atom
Atom: [[Math-Based Routines (np)]]
Topic: Quant
Understanding: #Exploratory 

----
# Order Statistics (Quantile & Percentile)

We have `np.percentile(a, q)` and `np.nanpercentile(a,q)` and `np.quantile(a,q)` and `np.nanquantile(a,q)`.  These require an `axis` input. Note `q` can be a scalar float or an array of floats e.g `q=[0.1,0.3.0.5,0.75]` to return the quantile cutoff value or values. 

# Moments (Up to 2nd)

These are aggregation functions and require an `axis`. We have `np.median(a)`, `np.average(a)`, `np.std(a)`, `np.var(a)`, and their `nan` versions.

# Correlation and Covariance

There are three functions - `np.corrcoef(a)` (correlation matrix) `np.cov(a)` (covariance matrix) and `np.correlate(a)` (cross-correlation).

# Histograms 

