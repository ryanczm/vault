Type: #atom
Subsubtopic: [[Portfolio Optimization (W)]]
Topic: Quant 
Understanding: #Exploratory Intuition

----
# Definition

Portfolio variance decomposition lets us **decompose the historical variance of a portfolio** into the contributions by individual alpha and risk factors and idiosyncratic risk.
# Exposure Vector

The exposure vector is the factor exposure matrix of the portfolio multiplied by the holdings vector $$e = B h$$ which is a vector containing the exposure to each factor of the portfolio ($B$ is $k$ factors by $n$ assets).

# Portfolio Variance Decomposition

Our expression for portfolio variance in terms of a risk factor model is $$\sigma^2_p=h^T\Sigma h=h^T(B^TFB+S)h = h^T(B^TFB)h+h^TSh$$
Substituting the exposure vector $e^T= (Bh)^T= h^TB^T$ we can get $$ h^T\Sigma h = e^TFe+ h^TSh$$
And dividng by the portfolio variance we can obtain a **variance decomposition**:  $$1= \frac{e^TFe}{h^T\Sigma H} + \frac{h^TSh}{h^T\Sigma H}= \sum_i^ke_i\frac{(Fe)_i}{h^T\Sigma H} + \frac{h^TSh}{h^T\Sigma H}$$Which decomposes the normalized portfolio variance (1) into the **sum of individual alpha and risk factor contributions** and **idiosyncratic variance**.

