Type: #atom
Subsubtopic: [[SciPy]]
Subtopic: Time Series
Topic: Statistics

----
# Overview

Interpolation uses **splines**. Splines are **piecewise polynomials**. In other words, simply create polynomials for each subset of the data, each with their own degree and parameters.

# Univariate Interpolation

Many options, but we usually use `CubicSpline(...)`. First, the object is instantiated with the `x` and `y` parameters. Then, we can feed it new `x` to produce the interpolated `y`.
