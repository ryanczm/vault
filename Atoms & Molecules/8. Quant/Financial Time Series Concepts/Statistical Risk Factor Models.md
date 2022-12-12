Type: #atom
Subsubtopic: [[Risk Factor Models]]
Topic: Quant 
Understanding: #Exploratory 

----
# Definition

Statistical risk factor models use PCA, which somehow maps PCA to the factor model.

* The **factor exposure/loadings/betas matrix** is the **principal components matrix**.
* The **factor returns matrix** is the **transformed returns matrix** $f=B^Tr$. Note even though $f$ is a matrix, it is not capitalized because $F=cov(F)$
* The **factor returns covariance matrix** is diagonal (factors are orthogonal)

Then we can use the factor model equation $r = Bf-s = BB^Tr-s$. Strange.

In AI4T, the task was to decompose returns with PCA into risk factors, and calculate factor returns over time (e.g 6 factor returns time series), but the course did not explain what to do with these factors.
