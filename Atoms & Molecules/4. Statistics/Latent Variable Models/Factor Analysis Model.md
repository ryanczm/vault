Type: #atom
Atom: [[Factor Analysis Fundamentals]] 
Subsubtopic: Latent Variable Models
Understanding: #Exploratory 

----
# Definition

Factor analysis is a statistical method that aims to estimate a model which explains variance/covariance between a **set of observed variables** by a set of **fewer unobserved (latent) factors** and their weightings.

Each observed variable is a **linear combination of weighted (loaded) factors** and an **error term** as a regression equation. There are $i$ observations (e.g 100 days of returns) for $j$ stocks (e.g 10 stocks) with $k$ factors.

This equation represents the model for the $i^{th}$ observation of the $j^{th}$ variable for the $k$ factors (e.g a return observation of one day of a particular stock in terms of two factors $k=2$): $$X_{ij}=\sum_{k}F_{ik}L_{kj}+ \epsilon_{ij}$$
Then we can express the above in matrix notation: $$X-M=FL+\epsilon$$where $X$ is $i \times j$, $F$ is $i \times k$ and $L$ is $k \times j$ and $\epsilon$ is $i \times j$. The goal is, given the observations $X$ and $F$, find the loadings matrix $L$ where each row is the factor loadings for the $k$ stock that minimizes error. 

# Estimation

The parameters are estimated by MLE or optimization.

# F.A vs O.L.S

If $F$ is known (usually unknown in conventional analysis except for number of factors), then isn't FA the same as running OLS on different $y$ variables? For example, in `sklearn.decomposition.FactorAnalysis`, the parameter `n_components` in the constructor assumes the factor values are unknown.

---
Factor analysis was invented in 1904 in a paper by Charles Spearman (1863-1945), 3 years later after Karl Pearson invented PCA in 1901.