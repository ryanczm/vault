Type: #atom
Atom: [[Interest Rates (Z)]]
Topic: Quant 
Level: #Exploratory 

----
# Overview

Time value of money refers to the idea that we can put money into the bank and **earn interest**, so to value money in the future or past, we must apply a discount factor. This factor comes from taking an **interest rate per annum** and stretching it out to continuous compounding (infinite compounding periods).

# Compounding Factor

If I invest $k$ now, I will get $k \cdot e^{rt}$ in $t$ years time. This is derived from $$(1+\frac{r}{m})^{mt} \sim e^{rt}$$where $r$ is an interest rate per annum offered by a bank, usually some float $0\leq r \leq 1$.

# Moving Money Backwards and Forwards

If I will get 1 dollar at time $T$ in the future, it's future value at earlier time $t$ is $e^{-r(T-t)}$.

