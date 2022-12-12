Type: #atom 
Subsubtopic: [[SciPy]]
Subtopic: Time Series
Topic: Statistics
Status: #incomplete 

----
# Overview

The `scipy.optimize` submodule contains classes for both **local** and **global** **(what is global optimization??)** optimization. Portfolio optimization is local.

In general, these require the passing of `fun`, an **objective function**. In specific cases, one can pass `fprime`, the gradient of the objective function. These also require other various specific keyword arguments.

# Scalar Functions Optimization (Of One Variable)

We have `scipy.optimize.minimize_scalar(fun, bracket, bounds, args, method)`.

# Scalar Function Multivariate Optimization

**Generic Interface** - `scipy.optimize.minimize(fun, x0, args, method)` - This is the generic interface. The `fun` has signature `fun(x, *args) -> float*` where `x` is a 1D NumPy array of weights. The function must return a float. The method is a string like `"L-BFGS-B"`.

**Specific Interface** - It also offers a method specific interface. In AI4T Ch8, they used `scipy.optimize.fmin_l_bfgs_b(fun, initial_guess, fprime)` . Note `fprime` is the gradient function of `fun`. Not sure of the specific differences.

# Global Optimization

# Root Finding

# (Mixed Integer) Programming Problems

