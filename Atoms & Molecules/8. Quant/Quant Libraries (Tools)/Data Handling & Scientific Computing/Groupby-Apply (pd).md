Type: #atom
Atom: [[Function Application (pd)]]
Topic: Quant 
Understanding: #Exploratory 

----
# Overview

The groupby apply workflow is function application on groups via the **split-apply (function)-combine method**.

It operates on a **groupby object taking in some function name** (either premade like `gb.apply(sum, axis=1)`

Unlike `df.apply(f, kwarg1=x, kwarg2=y)`, the groupby apply does not take in an axis, it is up to you to decide in the function. So it's very flexible.

Unlike `df.pipe(f, kwarg1=x, kwarg2=y)`, the groupby apply operates on individual groups.


1. **Splitting** - Splitting data into groups based on some criteria
2. **Applying** - Some function to each group.
3. **Combine** - Combining the results into a data structure.

# Groupby (Splitting)

The `groupby` method takes:

* `by` - The splitting variable, e.g a list of variables.
* `axis` - Rows or columns
* `level` - For MultiIndex.
* `group_keys` - exclude keys if grouped. Not that important.

# Applying

**Applying Functions on Each Group** - The `.apply(func)` method is the most flexible way of doing something on a `groupby` object, because `func` can return a `DataFrame`, `Series` or `scalar`. For example, in TM capital's last question, we could easily have created a function that de-ages and then applies regression to return the beta and intercept coefficients, then put it into `GroupBy.apply(func, kwarg1=x, kwarg2=y)` for an easy answer.

**Piping vs Applying** - [Stackoverflow - Pipe vs Apply](https://stackoverflow.com/questions/47226407/pandas-groupby-pipe-vs-apply)