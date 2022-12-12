Type: #atom
Atom: [[Indexing (pd)]]
Topic: Quant 
Understanding: #Exploratory 

----
# Multi-Indexing

Operations on MultiIndex objects in Pandas require the specification of a level. Note each MultiIndex is a tuple of values.

**Constructors** 

`pd.MultiIndex.from_arrays()`, `pd.MultiIndex.from_tuples()`, `pd.MultiIndex.from_product()`, `pd.MultiIndex.from_frame()`.

**Components**

Sorting - We can use the `.sortlevel()` method to return the sorted index at the specified level.
Dropping - We can drop a level by using the `.droplevel()` method.
Swapping Levels - We can swap levels by using the  `.swaplevel()` method

# Slcing a MultiIndex

The idea is to pass in MultiIndex values as input into `.loc[]`.

Using **IndexSlice** - `df.loc[pd.IndexSlice['AAPL',:],:]` . The `IndexSlice` object lets you produce a slice of the index. Common convention is to create the object with an empty constructor like `idx = pd.IndexSlice` then use `df.loc[idx[:,:],:]`.

Using xs (cross-section) - [!]


