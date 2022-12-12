Type: #atom
Subsubtopic: [[SciPy]]
Subtopic: Time Series
Topic: Statistics

----
# Overview

It is mentioned in the docs these try to avoid covering existing statistics from `statsmodels`.

# Probability Distributions

Methods - After instantiating the distribution (E.g `scipy.stats.norm(loc=10, scale=10)`), these are the some useful methods:

* d.rvs() - Generates the r.v
* d.pdf(...) - Generates the probability
* d.cdf(...) - Generates cumulative probability
* d.stats(...) - Generates moments
* d.entropy(...) - Generates differential entropy
* d.fit(...) - Fits via MLE, returns parameter tuple
* etc

# Summary Statistics (Nonparametric)

# Correlation Functions

These are important. Common ones include `scipy.stats.pearsonr(...)` and `scipy.stats.spearmanr(...)`.

# Statistical Tests

We have t-tests, chi-square tests, KS tests, Jarque-Bera tests, 