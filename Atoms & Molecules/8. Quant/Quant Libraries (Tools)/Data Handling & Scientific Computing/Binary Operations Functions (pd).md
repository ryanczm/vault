Type: #atom
Atom: [[Computations & Stats (pd)]]
Topic: Quant 
Understanding: #Exploratory 

----
# Overview

Binary operations are things like `.pow()`, `.sub()`, `.add()` etc. Their input can be a scalar (operation done element wise) or a `Series` - e.g add a `Series` to a `DataFrame`. If the latter, an `axis=1` or `axis=0` must be specified to do the operation.

We can also use the overloaded arithmetic operators like `*`, but if we need to specify the axis, we have to use the corresponding binary operation method.

The key idea is that they are **axis-specific**.