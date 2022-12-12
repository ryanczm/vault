Type: #keyatom 
Atom: [[Risk]]
Topic: Quant 
Understanding: #Exploratory 

----
## Definition

A **risk measure** can be used by an institution to make an investment decision. In buy-side, funds use a risk measure to determine if a portfolio's allocation exceeds a certain risk tolerance to adjust weights. For now, just think of it is a **scalar quantifying how bad things can go** (volatility does not quantify direction).

[!] **How is a risk measure used in portfolio optimization**? In AI4T, the constraint is portfolio variance, which is not a risk measure (it is called a **deviation risk measure**). How would **value-at-risk** be used in portfolio optimization?

# Properties

A risk measure has certain properties - it is **normalized (?)**, **translative (?)** and **monotone (?)**. Apparently, because volatility **does not** satisfy the translation and monotonicity property, it is not a **risk measure**.

# Examples of Risk Measures

Examples of risk measures are **value-at-risk**, **expected shortfall**, **entropic value-at-risk**, **drawdown** & **tail conditional expectation**.