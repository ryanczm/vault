Type: #atom
Subsubtopic: [[Alpha Factor Preprocessing]]
Topic: Quant 
Understanding: #Exploratory  Understanding

----
# Z-Scoring

Z-scoring refers to the process of demeaning the alpha vector and then dividing by standard deviation. Assuming the data follows a normal distribution, this operation converts the vector to z-scores. However, z-scoring is **not robust to outliers**.

A common method is to **rank first**, then **z-score the rank**. Note z-scoring across the entire vector makes the alpha vector dollar-neutral.

# Z-Scoring Demeans the Factor

It is important to note z-scoring demeans the factor, meaning it sums to 0. 