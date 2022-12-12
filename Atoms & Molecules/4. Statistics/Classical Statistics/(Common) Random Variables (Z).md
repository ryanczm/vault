Type: #atom
Atom: [[Random Variables & their Distributions (B)]]
Subtopic: Classical Statistics
Topic: Statistics
Understanding: #Exploratory Intuition

----
# Overview 

The formal definition of a **random variable (RV)** is a **mapping from sample space to the real line**.

The **probability function (probability density function)** of the random variable maps from the real line to probability. We can visualize it adding a **height dimension to the real line**. PDFs are parameterized by the variable itself, $x$ (the outcome on the real line), and some parameters, $\Theta$.

This note showcases the summary table from *Zhou's The Green Book*, explaining some commonly used distributions & their interpretation

# Common Discrete Distributions

The discrete uniform distribution is an even roll. The binomial variable represents number of successes of $n$ Bernoulli trials with probability $p$. The Poisson r.v represents the number of events occuring in a fixed period of time with fixed rate $\lambda$ events per implicit time. The geometric r.v represents the trial number $n$ to get the first success. The negative binomial represents the trial number to get the $r^{th}$ success. The hypergeometric represents trial number to get the $r^{th}$ success from $k$ trials without replacement.

![[common_discrete_variables.png]]

# Common Continuous Distributions

The exponential distribution represents the arrival time of an event if it has a constant arrival rate $\lambda$. The gamma $(\alpha, \lambda)$ is the distribution of amount of time one waits for $n$ events to occur. The Beta distribution is used to model events constrained by the interval $[0,1]$.

![[common_continuous_variables.png]]