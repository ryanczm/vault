Type: #atom
Atom: [[Random Variables & their Distributions (B)]]
Subtopic: Classical Statistics
Topic: Statistics
Understanding: #Exploratory Intuition

----
# Overview 

This note details how **random variable moments** are like for **linear transformations** (e.g linear combinations - scaling and addition). So if $X,Y$ are random variables, a linear transformation would be something like $4X-3Y$. This behavior only holds for linear operations! An example of a nonlinear operation is, say, a power, like $X^2$. This note is rules for the former.

# First Moment - Expectation

Expectation of any **linear transformation** of RVs, is **linear in itself**, **regardless if the RVs themselves are independent or dependent**. So it directly follows linear operations: $E(4X-3Y)=4E(X)-3E(Y)$. 

# Second Moment - Variance and Standard Deviation

Variance is somewhat linear under linear transformations - but if two RVs are not independent, then a covariance term will pop up.

Scaling by a Constant - Because variance has a square, any scaling must be squared to move it outside the variance operator: $Var(aX)=a^2Var(X)$. As a result, the square means subtraction of random variables still increases overall variance.

Subtraction and Addition - Subtraction and addition yield the same results (if independent) $var(X+Y)=var(X-Y)=var(X)+var(Y)$. If dependent, then the former special case generalizes to the general case with covariance included (now sign-dependent): $$Var(aX\pm bY)= a^2Var(X)+b^2Var(y) \pm 2ab\space Cov(X,Y)$$
For standard deviation, simply conduct the variance operation, then square the answer.

Another common trick is subtraction or addition of a constant $Var(X-c)=Var(X)$ - shifting a distribution leaves the variance unchanged.