Type: #keyatom 
Subsubtopic: [[Volatility Models]]
Subtopic: Time Series
Status: #incomplete 
Topic: Statistics

----
The goal of C.H models is to estimate $\sigma_t^2$ - the current or lookahead variance based off a log return series.

The key intuition for $ARCH(m)$ is we use a weighted sum of squared log returns similar to EMWA fashion. However, the weight vector $\{\alpha\}=a_i + \cdots + \alpha_m$ are the model parameters  to be estimated.

The key intuition for $GARCH(m,n)$ is that it is a weighted sum of squared log returns and also weighted sum of historical volatilities. The $\alpha$ vector is the weights of the returns and $\beta$ vector is the weights of historical volatilities.


