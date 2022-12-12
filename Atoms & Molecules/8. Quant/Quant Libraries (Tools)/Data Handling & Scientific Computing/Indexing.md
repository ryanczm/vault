Type: #atom
Atom: [[Indexing (pd)]]
Topic: Quant 
Understanding: #Exploratory 

----

# Multiple Value Indexing

Explicit Slicing - We can use the `.loc[]` method. Allowed inputs are a single label, a list of labels, a slice object (e.g `'a':'f'`, a **Boolean array**, a **Boolean series** (created from a **masking operation** like an inequality operator), and an **index object** (often sliced).

Implicit Slicing - We can use the `.iloc[]` method.

# Single Value Indexing

Explicit Single Value - We can use `.at[]`  a single value.
Implicit Single Value - We can use `.iat` which requires integer inputs.

# Getting Location

Getting Single Location - Use `.get_loc()` which takes in a value and returns the index of those values.
Getting Sequenced Location - Use `.get_locs()` which takes in values and returns the index of those values.

# Indexing Objects

These are the index objects in Pandas: `Index`, `NumericaIndex`, `CategoricalIndex`, `IntervalIndex`, `DateTimeIndex`, `TimedeltaIndex`, `Periodindex` and `MultiIndex`.

These can all be input into a `.loc[]` to slice and filter Each of them have their own methods and attributes.

