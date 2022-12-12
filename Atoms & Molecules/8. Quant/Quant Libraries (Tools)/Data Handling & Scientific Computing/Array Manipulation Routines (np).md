Type: #atom
Atom: [[Creation & Manip. Routines (Np)]]
Topic: Quant
Understanding: #Exploratory 

----
# Overview

Array manipulation routines are concerned with changing the shape and size of arrays. Many of these have similar API to PyTorch (since PyTorch was built on NumPy).

# Dimension and Axis Primer

Consider an array of shape `(2,3,3)`. Read from right to left. Each dimension multiplies the previous one. So 3 first, then 3 of 3, then 2 of 3 of 3. The axis is 0 indexed.

Passing a tuple of axes e.g `(1,0)` in a routine like `sum` amounts to applying the function on the first axis, then the second

# Changing Array Shape

These accept an additional option, `order=C`. 

Reshaping - Using `np.reshape(a, newshape)` to cast into new shape. Alternatively, consider `a.reshape(newshape)`. 
Ravel - Flattens the array into a 1D array. This is equivalent to `a.reshape(-1)`.
Flatten - Also flattens via `a.flatten()`.

# Changing Dimensions [!]

Expand Dim
Squeeze

# Joining Arrays [!]

This stuff is very confusing.

Concatenation
Vstack
Hstack
Dstack

# Splitting Arrays [!]

# Tiling Arrays [!]

# Adding & Removing Elements [!]

# Rearranging Elements [!]