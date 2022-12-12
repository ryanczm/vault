Type: #atom
Atom: [[Expectation & Variance (B)]]
Subtopic: Classical Statistics
Topic: Statistics
Understanding: #Exploratory Intuition

----
# Overview 

The LOTUS describes the expectation of a function of a random variable, $E(g(X))$, and says it is possible to calculate this just using $X$ itself!

First, expectation is defined as $E(X)=\sum_x x p_x$ in the discrete case or $\int x f(x) dx$ in the continuous case. Then the LOTUS states we can simply change the $x$ to $g(x)$ to get $E(g(X))$ - the expectation of the function of the RV: $$E[g(X)]=\sum_xg(x)p(x)=\int_{-\infty}^{\infty}g(x)f(x)dx$$For example, for $E(X^2)$, we can use LOTUS with $g(x)=x^2$.