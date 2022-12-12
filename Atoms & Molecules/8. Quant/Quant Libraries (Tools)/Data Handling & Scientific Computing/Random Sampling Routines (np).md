Type: #atom
Atom: [[Math-Based Routines (np)]]
Topic: Quant
Understanding: #Exploratory 

----
# Overview

These are for generating random samples drawn from some probability distribution. The namespace is `np.random`. The `size` parameter is a tuple of ints specifying the shape of the sample `ndarray`.

`np.random.normal(loc, scale, size)` for the Gaussian distribution. Numpy only offers random variable generation. `scipy.stats` offers more functionality (e.g pdf, cdf).