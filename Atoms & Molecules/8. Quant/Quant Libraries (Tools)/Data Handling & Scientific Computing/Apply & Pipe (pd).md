Type: #atom
Atom: [[Function Application (pd)]]
Topic: Quant 
Understanding: #Exploratory 

----
# Apply

The apply method operates on a dataframe object and applies the function over a specified axis. Unlike groupby.apply, there is no SAC or splitting into groups involved - `df.apply(f, axis=0)`

# Pipe

The pipe method operates on a dataframe object but applies the function generally, just like groupby-apply. No axis is involved. This allows for method chaining: `df.pipe(g).pipe(f)`.


