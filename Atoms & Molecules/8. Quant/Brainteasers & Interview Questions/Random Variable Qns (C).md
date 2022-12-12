Type: #atom
Atom: [[Probability & Stats Qns (C)]]
Topic: Quant 
Status: #inprogress 
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



