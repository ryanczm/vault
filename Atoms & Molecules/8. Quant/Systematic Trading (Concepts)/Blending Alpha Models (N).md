Type: #atom
Atom: [[Alphas & Signals (W)]]
Topic: Quant
Understanding: #Exploratory 

----
An alpha model produces signals to take positions in either a single or multiple security - but can be **blended together** (assigning weights to signals operating on the same assets). E.g in case of conflicting signals from two alpha models on the same security. Blending can be **linear**, **non-linear** or **machine learning**. The key idea is that alphas are just position/decisions and can be combined.

## Linear Blending

In **linear blending**, signals are blended based on a **linear combination of weighted signals**, whereby weights are derived from linear regression (how?). E.g if a value strategy on E/P ratio predicts +20% return in next 12 months for XOM and a trend model predicts -10% for the same time period, we can weigh them 70-30 to produce a **composite signal**.

## Nonlinear Blending

Narang details two different ways of **nonlinear blending** - **conditional variables** or **rotation approach**.

In the conditional variable approach - we have internal conditioning variables - e.g only consider the signal if both models are in agreement or external conditioning variables - weigh one model more if some external variable is above a certain level, 

* E.g consider a mean reverting stat arb strategy. Some practitioners believe stat arb works better when market volatility is high. Then, volatility is the c.v to overweight the stat arb strategy relative to others.

