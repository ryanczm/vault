Type: #atom
Atom: [[Split-Apply-Combine (pd)]]
Topic: Quant 
Understanding: #Exploratory 

----
# Overview

Groupby refers to a process involving these general steps:

1. **Splitting** - Splitting data into groups based on some criteria
2. **Applying** - Some function to each group.
3. **Combine** - Combining the results into a data structure.

We can think of the group by step as a splitting step that partitions the data by some categorical variable. Within the apply step, we can **aggregate**, **transform** or **filter**.

# Groupby (Splitting)

The `groupby` method takes:

* by - The splitting variable, e.g a list of variables.
* axis - Rows or columns
* level - For MultiIndex.
* group_keys - exclude keys if grouped. Not that important.

# Applying

**Applying Functions on Each Group** - The `.apply(func)` method is the most flexible way of doing something on a groupby object, because `func` can return a `DataFrame`, `Series` or `scalar`. For example, in TM capital's last question, we could easily have created a function that de-ages and then applies regression to return the beta and intercept coefficients, then put it into `GroupBy.apply(func)` for an easy answer.

**Piping on the Whole DataFrame** - The pipe function is applied to a `GroupBy` or `DataFrame` object but operates on global scope, not per sliced group which `.apply(func)` does. So `df.pipe(lambda x: x)` would end up applying the function to the entire global scope.
