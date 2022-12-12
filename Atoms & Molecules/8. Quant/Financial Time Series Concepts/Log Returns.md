Type: #atom
Atom: [[Arithmetic & Geometric Return]]
Topic: Quant
Understanding: #Exploratory 

----
We can use the **time additivity property** of logarithmic returns for easier computation: $$\begin{gathered}\ln(\prod (1+r_i))=\sum \ln(1+r_i)\\ =\sum \ln\frac{p_n}{p_n-1}\\=\ln (p_n)-ln(p_0) = ln\frac{p_{t}}{p_{t-1}}\end{gathered}$$
To convert from raw returns to log returns, we have $$R= \ln(r+1)$$ and $$r=e^{R}-1$$In Pandas:

```Python
SP500['R'] = np.log(SP500['r']) - np.log(SP500['r'].shift(1))
# or we can use this method
SP500['R'] = np.log(SP500['R'].pct_change(1) + 1)
```


---
Source: [Gregory Gundersen - Log Returns](https://gregorygundersen.com/blog/2022/02/06/log-returns/)
