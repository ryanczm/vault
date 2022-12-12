Type: #atom 
Subsubtopic: [[Optimization Formulation with Alpha & Risk Models (W)]]
Topic: Quant 
Understanding: #Exploratory Intuition

----
# Definition

In a portfolio optimization problem constraints can either be put explicitly or **put into the objective function**. Apparently, constraints slow down the optimizer, so it is best to put them directly. 

This note contains several concepts and strategies from AI4T Transaction Cost lessons to **improve computation speed of portfolio optimization.**

# Conversion from Constraint into Objective Function

Hence, each of the **constraints** (e.g leverage, position size, common risk, specific risk) can be **converted** into a form that can be put in the objective function via **some process**.

* A market neutral **constraint** (dollar-neutral) ⇔ **minimizing** common risk (market risk).
* A total position size **constraint** (leverage) ⇔ risk aversion **parameter** (controls portfolio size).
* An individual position size **constraint** ⇔ minimizing specific risk (idiosyncratic risk) of an individual asset.

# Shrinkage of Covariance Matrices

Apparently, shrinkage is good. Not sure why. Shrinkage of off-diagonals to 0 is also good for computation speed.

# Breaking Up the Risk Factor Component of Objective Function for Speed

$BFB^T + S$ is a $n \times n$ large covariance matrix and calculation is computationally intensive. Apparently, we can use some matrix factorization methods to compute $h^T (BFB^T+S) h$ more efficiently. Let $F=GG$. Then, $BFB^T=BGGB^T$. Then, let $Q=GB^T$. Then, $BFB^T=BGGB^T=Q^TQ$. We use this expression instead.

Now $h^T(Q^TQ)h=R^TR$ where $R=QH$. We want to avoid creating square matrices because $\mathcal{O}(n^2)$ is bad. Notice how $R$ is a vector. 


# Risk Aversion Parameter

A risk aversion parameter $\kappa$ can be put into the objective function that corresponds to the holding size of the portfolio (corresponds to leverage constraint).
