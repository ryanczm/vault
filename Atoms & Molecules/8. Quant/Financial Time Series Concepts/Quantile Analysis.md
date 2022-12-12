Type: #atom
Atom: [[Performance Measurements]]
Topic: Quant 
Understanding: #Basic Understanding

----
# Definition

**Quantile analysis** refers to **bucketing the sorted alpha vector** into quantiles of instruments based on the **cumulative alpha values over time**. Then, within each quantile, we calculate the quantile **mean** and **standard deviation** of the **return as a boxplot**. 

Ideally, we should see monotonic relationship with quantiles and returns. If we don't see this, it indicates the factor might have issues. The higher the alpha vector quantile, the higher the return.