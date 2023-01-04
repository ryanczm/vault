Type: #atom
Atom: [[Probability & Stats Qns (CZ)]]
Topic: Quant  
Level: #Exploratory 

----
# Product of Two Uniformly Distributed Random Variables Qn (4.2)

Q: Suppose we draw two random numbers $X$ and $Y$ each $Uni[0,1]$. What is the probability that their product is greater than $1/2$?
A: This actually doesn't need any knowledge of uniform PDFs and moments. Simply imagine a unit square. Then, $xy > 1/2 \rightarrow y > \frac{1}{2x}$. So we need that quadrant shaped area on the unit square above the intersection of   $y=\frac{1}{2x}$. Anyway, at $y=1$, $x=0.5$ and at $x=1$, $y=0.5$. So the area is somewhat a curved triangle (quadrant), approx 0.125 or 1/8 probability.
A: Alternatively, the area is $1/2 - \int_{1/2}^1 \frac{1}{2x}dx$.

# PDF of Gaussian RV Qn (4.3)

Q: Write down the PDF of Gaussian R.V. Where does the constant factor come from?
A: Constant factor is to scale the Gaussian integral so the area scales to 1.

# Expectation of Squared Gaussian RV Qn (4.4)

Q: What is $E(X^2)$ of a Gaussian random variable?
A: The answer is to use the variance formulation: $E(X^2)=Var(X)+(E(X))^2$

# Standard Deviation of X-Y Gaussian RV Qn (4.5)

Q: As above, if $X,Y$ are $Z$ distributed, what is the standard deviation of $X-Y$?
A: It is, using linear combinations of R.V identities for variance, $\sqrt{(\sigma_x^2 + \sigma_y^2)}=\sqrt{2}$.

# Correlation of Scaled RVs Qn (4.9)

Q: Correlation between $X,Y$ is $\rho$. What is correlation of $X+5,Y$ or $5X,Y$?
A: Shifting does nothing to correlation. Scaling also does nothing (write out correlation formula to see, numerator is scaled by 5, denominator is scaled by square root of 25).

# Expected Value of Lognormally Distributed RV Qn  (4.33)

Q: If $X$ is Gaussian, what is $E(e^X)$?
A: The answer is to use LOTUS, the Gaussian pdf and completing the square in the integral to solve, or using MGFs, which is $E(e^X)=e^{\sigma + \frac{1}{2}\mu^2}$.

# Write Down CLT Qn (4.58)

Q: Write down the CLT.
A: There are many variants, usually implicit is the univariate (wow there's a multivariate case) Lindberg-Levy CLT (canonical). The standardized sample mean of i.i.d r.vs with $\mu$ and $\sigma$ is a standard normal distribution with $\sigma_{\bar{X}}=\sigma/\sqrt{n}$

# Making Two Uncorrelated Gaussian's Correlated ((4.59)

Q: Given two uncorrelated Gaussian r.vs $Z_1$ and $Z_2$, how can you obtain two correlated Gaussian r.vs $X_1, X_2$ with correlation $\rho$?
A: Simply simulate the data $D$ then apply a special covariance matrix $\Sigma$ to $\Sigma D$ to reshape the data.

# Triangle & Stick Breaking Problem (4.40)

Q: Take a stick and randomly break it into three pieces (2 random breaks on stick). What is probability you can form triangle from pieces?
A: The trick is triangle inequality: $x+y \geq z$. A stick is partitioned into $(x,y,1-x-y)$. Non-negativity implies each piece is positive. Rearrange to get $x+y \leq 1$. Now, this forms a triangle in $x,y$ plane, from $y=1$, $x=1$. Now, applying triangle inequality: we require $x\geq 1/2$, $y \geq 1/2$ and $x+y \geq 1/2$. This forms a mini triangle within the triangle with $1/4$ area. So probability is $1/4$. This solution is gimmicky. The actual solution in book is for an $n$-edge polygon.

# Meeting Under the Clock Problem (Probability of Meeting in a Window) (4.45)

Q: We agree to meet under a big clock at the train station, between 1PM and 2PM. Each of us will wait no more than 15 minutes for each other. We will arrive precisely in between 1PM and 2PM. What is the probability we will meet?
A: We draw the time on the cartesian plane, from 1.00 to 2.00 pm. Then, we start at 1.15pm on both axes, and draw a $y=x$ line upwards. The area shaded is 7/16.