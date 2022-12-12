Type: #atom
Subsubtopic: [[Alpha Factor Preprocessing]]
Topic: Quant 
Understanding: #Exploratory  Understanding

----
# Neutralizing

Cross-sectional alpha factors can be engineered to reduce exposure to risk factors.

## Market Risk - Dollar Neutralization

To neutralize an alpha vector for market risk, simply perform **dollar-neutralization** - demean it with the global mean

## Sector Risk - Sector Neutralization

To neutralize an alpha vector for sector risk, simply perform **sector neutralization** - demean the alphas for stocks within a sector by the sector-specific mean. This can be done for all sectors in addition to **dollar neutralization**.

For example, if the alpha factor is the 1-year return, then we first have to compute 1-year returns via a `zipeline` `returns` factor, then perform sector neutralization with a `zipline` `classifier` object.