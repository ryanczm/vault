Type: #atom
Atom: [[Date and Time Series (pd)]]
Topic: Quant 
Understanding: #Exploratory 

----
# Overview

These methods return window objects and a method can be called on them. The key intuition is that the returned output is the **same shape** as the original dataframe.

To create the object, we use `df.rolling(..)`, `df.expanding(...)`, `df.ewm(...)`.