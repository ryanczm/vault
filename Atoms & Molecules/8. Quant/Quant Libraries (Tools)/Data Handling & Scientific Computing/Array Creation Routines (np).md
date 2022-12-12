Type: #atom
Atom: [[Creation & Manip. Routines (Np)]]
Topic: Quant 
Understanding: #Exploratory 

----
# Overview

Array creation routines refer to building `ndarrays`, be it vectors, matrices or tensors in a convenient fashion.

# Creation from Python Arrays

The standard `np.array()` works. The input is a (nested) `list`. Note the number of dimensions is the longest number of brackets on the outside, e.g `np.array([[[1, 2], [3, 4]], [[5, 6], [7, 8]]])`  will create a `3D` array of shape `(2,2,2)`.

# Creation from Shape or Value

## 1D Array Creation

These are `np.arange()` (define by step size) and `np.linspace()` (define by number of steps).  These require `start`, `stop`. `arange()` requires `step` and `linspace()` requires `num`.

## 2D Array Creation 

Diagonal - `np.diag()` constructs a diagonal matrix from a `1D` array.

## General Creation

These often require to input dimensions as `shape` via tuple like `(3,3)`. The `_like` methods take in another array as input and create an array of values with same shape as input, e.g `np.ones_like(x)` .

Empty - `np.empty`  creates uninitialized arrays, just grabbing a block of memory randomly.
Identity - `np.eye`  and `np.identity` creates identity matrices.
Ones and Zeros - `np.ones` and `np.zeros`
Custom Fill Value - `np.full` with a specified `fill_value`

