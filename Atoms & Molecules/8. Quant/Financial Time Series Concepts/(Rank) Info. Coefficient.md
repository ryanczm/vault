Type: #atom
Atom: [[Performance Measurements]]
Topic: Quant 
Understanding: #Basic Understanding

----
# Definition

The **rank information coefficient** is a measure used to evaluate the **relative skill of an alpha vector across time**. Given an **ranked alpha vector** and **ranked forward returns** for that alpha vector, the rank i.c is the **Spearman rank correlation coefficient** between the two.

A high rank i.c close to 1 means the ranks of the alpha vector correlated with the ranks of the forward returns for that time period. 

We can repeat the rank i.c calculation for all time periods to get a **rank i.c time series** which shows the **skill of the alpha factor evolving over time**. Ideally, it should be as close to 1 over time as possible.

# Why Spearman over Pearson for Alpha Vector Evaluation?

Spearman ignores magnitude. We don't care about being wrong in terms of magnitude, but rather direction. Consider the top ranked alpha value for a stock and top return. If the magnitude of return is far higher than the alpha value, then Pearson's correlation will be low but Spearman's correlation will be high. 