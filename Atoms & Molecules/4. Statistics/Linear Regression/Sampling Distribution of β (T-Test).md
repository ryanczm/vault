  Type: #atom
Atom: [[Cov. Matrix of β]]
Subsubtopic: OLS Estimation
Understanding: #Exploratory Intuition

----
# Overview

The null-hypothesis is $H_0=\beta_p=b_p$, where $b_p$ is the true value for the $p^{th}$ coefficient and the alternative hypothesis is $H_1=\beta_p \neq b_p$. Then if the p-value is small, it is unlikely the estimate $\hat{\beta_p}$ occured by chance.
The *sampling error*, is normally distributed **(proof skipped)**: $$\hat{\beta}_p - b_p \sim\mathcal{N}(0,\sigma^2[(X^TX)^{-1}]_{pp})$$
Where $X^TX$ is the Gram matrix and $\sigma^2$ is the population variance of the errors $e$ (assuming spherical variance). We estimate the sample variance of errors as $s^2$. $$s^2=\frac{e^Te}{N-P}$$ Then we can normalize the sampling error by the standard error of the sampling distribution: $$SE(\hat{\beta}_p)=\sqrt{s^2}[(X^TX)^{-1}]_{pp}$$ to give us the test statistic that is $T$-distributed (**proof skipped**): $$T_0=\frac{\hat{\beta}-\beta}{SE(\hat\beta)} \sim t(N-P)$$
With $N-P$ (number of samples - predictors) d.f. Then if the t-statistic is sufficiently extreme, based on either really high sample variance of residuals: we can conclude the null hypothesis is false - that the OLS estimator coefficient is not statistically significant.


----
Source: [Gregory Gundersen - OLS Hypothesis Testing](https://gregorygundersen.com/blog/2021/09/09/ols-hypothesis-testing/)