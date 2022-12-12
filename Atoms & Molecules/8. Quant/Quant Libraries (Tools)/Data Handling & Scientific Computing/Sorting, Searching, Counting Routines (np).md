Type: #atom
Atom: [[Misc Routines (np)]]
Topic: Quant 
Understanding: #Exploratory 

----
# Overview

These methods require `axis` input to compute over.

# Sorting

The main ones we use are `np.sort(a)` and `np.argsort(a)`. The latter sorts then converts to indices.

# Searching

Where - This is equivalent to a vectorized if-else replacement operation. `np.where(condition, t,f)`. `condition` is a broadcasted Boolean expression like `x >= 5`, `t` and `f` are the arrays to replace in.

Argmax and Argmin - These find the indices of the max/min over an axis. So `np.argmax(a)` and `np.argmin(a)`


