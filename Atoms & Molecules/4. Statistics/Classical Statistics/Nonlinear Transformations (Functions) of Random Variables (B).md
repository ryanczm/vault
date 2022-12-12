Type: #atom
Atom: [[Random Variables & their Distributions (B)]]
Subtopic: Classical Statistics
Topic: Statistics
Status: #inprogress 
Understanding: #Exploratory Intuition

----
# Overview 

Nonlinear transformations refer to things like: raising to a power e.g $X^2$ and exponentiation e.g $e^{aX+b}$. In Blitzstein, these are also referred to as functions of random variables. We can use LOTUS to find expectation.

# Squared Case or Power Case

Many times, we are asked to find $E(X^2)$.  This arises in the variance formula: $E(X^2)=Var(X)+(E[X])^2$. What about for higher powers? Not sure.

# Exponent Case

What about $E(e^X)$? Well, this has 3 related concepts. It can be evaluated with MGFs or LOTUS (same result), and is linked to the lognormal distribution. [An example using LOTUS is here](https://math.stackexchange.com/questions/176196/calculate-the-expected-value-of-y-ex-where-x-sim-n-mu-sigma2).

The moment generating function of a normally distributed variable is $M_X(t)=e^{\mu t}e^{\frac{1}{2}\sigma^2 t^2}$. We can set $M_X(1)$ to get the desired result.