Type: #atom
Subsubtopic: [[Cross-Sectional Models (sm)]]
Subtopic: Time Series
Topic: Statistics
Understanding: #Exploratory 

----
# Overview

Statsmodels offers OLS, WLS, GLS, and Rolling OLS.  The default methodology is to instantiate first:

**Endog** - 1d array of Y variables.
**Exog** - X. By default, always use `X = sm.add_constant(X)` to add the intercep.

Then we can `r = m.fit()` the model which returns a `RegressionResults` object. 

# Results

The `RegressionResults` object has a wide variety of methods and attributes. Examples include `r.summary()` and `r.params`. Other examples include `r.aic`, `r.bic`, `r.rsquared`, `r.ssr`, `r.tvalues`, `r.fvalue`, `r.resid`, etc etc.

# Rolling OLS

The `sm.RollingOLS(...)` requires a `window` parameter for the length of the window. We can access the `params` attribute of `RollingRegressionResults`, in this case, the betas should be of shape `n-w, k` where `w` is window length.