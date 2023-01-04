Type: #atom
Atom: [[The Random Behavior of Assets (W)]]
Topic: Quant 
Status: #inprogress   
Level: #Exploratory 

----
# Constructing a Random Walk Model for Asset Prices

The purpose of a random walk model is to be able to 'analytically' simulate a series of values that 'looks' like an asset price: $$R_i=\mu \space \delta t + \sigma \space \phi\space (\delta t)^{1/2}$$
Our return is decomposed by a drift term (which scales by $\mu \cdot \delta t$ - scale mean linearly with **single time step**) and a volatility term which scales with square root of **single time step length**. 

Now, $\mu$ and $\sigma$ are parameters of the model which are estimated from mean and standard deviation of the asset return series. With some rearrangements using return formula: $$S_{i+1}=S_i(1+\mu \space \delta t+ \sigma \phi \space (\delta t)^{1/2}) \quad \quad S_{i+1}-S_i=\mu \space S_i \space \delta t + \sigma \space \phi\space S_i \space  (\delta t)^{1/2}$$
Remember, it is the sum of variables.

# Wiener Process

1. Starts from 0
2. Has independent increments
3. Gaussian increments that scale with square root of the interval of the increment: $W_{t+u}-W_t \sim \mathcal{N}(0, u)$
4. The limit of a random walk with normally distributed increments.

# Geometric Brownian Motion

The equation for a GBM (asset model) is a stochastic process, with a drift term and a stochastic term that follows a Wiener process (Brownian motion) $$dS=\mu S \space dt + \sigma \space S \space dW_t$$Now, this is an SDE. the $W_t$ is the Wiener process. Positive drift means the process goes upwards overall.

A GBM is a LRW, a geometric brownian motion is a lognormal random walk. 

# Solution to the GBM SDE

The solution to the GBM SDE is:  $S_t=S_0e^X$. Where $$X=\sigma W_t+(\mu - \frac{1}{2}\sigma^2) t$$
```Python
def gbm(T, mu, sigma, s0, dt=1.0, num_steps=1000):
	t = np.linspace(0, T, num_steps+1) # array of time intervals
	W = np.random.standard_normal(size=num_steps+1) # increments
	w = np.cumsum(w) * np.sqrt(dt) # Brownian motion
	X = (mu - 0.5 * sigma ** 2) * t + sigma * w
	S = s0 * np.exp(X)
	return S
```
