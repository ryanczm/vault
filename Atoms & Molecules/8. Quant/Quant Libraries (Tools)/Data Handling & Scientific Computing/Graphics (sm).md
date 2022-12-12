Type: #atom
Subsubtopic: [[Cross-Sectional Models (sm)]]
Subtopic: Time Series
Topic: Statistics
Understanding: #Exploratory 

----
# QQ-Plot

A quantile-quantile plot is used to show empirically how well some data fits a reference univariate distribution.

The call returns a `figure`. Use case is `fig = sm.qqplot(data, dist, distargs, loc, scale, fit)`. The `dist` is a `scipy.stats.norm` by default (standard normal), but we can input some `scipy.stats` distribution object. 

The `distargs` is a tuple like `(4,)` which is any parameter into the `scipy.stats` distribution that is not `loc` and `scale`. The `fit=False` is a Boolean, if `True`, it will fit the distribution.

