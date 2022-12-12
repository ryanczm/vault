Type: #topic

---
## The Central Problem of Quant Trading

Trading is simply a process - a **series of decisions** to be made in future time. A **decision** is simply a **position**.

* What to buy/sell (asset)
* When to buy/sell (time)
* How much to buy/sell (quantity)
* What criterion to optimize (objective)
* Who does it (participants)

These decisions are made by some **strategy**:

* Some **data** (time period, asset class, nature of data) 
* Some **algorithm** (technique) to process the data to produce a decision - which has a quantitative spectrum (slightly quantitative to very quantitative).

Which implements these decisions by submitting them to an **exchange**. Fixing the asset, that forms a **strategy**. A single entity doing this for a range of different assets constitutes a **portfolio**. A strategy is a individual piece, and the **portfolio** composes the jigsaw. The purpose of the strategy is to reduce the variety of choices.

## Infinite Possibilities (High Dimensional Decision Space)

To get an idea of the scale of the complexity - we can multiply these together to have a huge number of possibilities:

**Number of assets** - There are multiple exchange-traded asset classes (equities, debt, derivatives, currencies). In equities alone, there are ~41,000 listed stocks. In bonds, there are ~500,000 unique corporate bonds in the US alone.

**Time** - Consider the amount of permutations of time periods (from the millisecond, to minute, to hour, to day, to weeks, to months) and the number of intervals within each time period. 

**Quantity** - There are thousands of quantities one can buy at.

**Data** - Consider the vast amount of types of data out there.

**Algorithms/Strategies** - Consider the vast amount of algorithms/strategies, for each asset class, for each time period, for each quantity, for each type of data.

**Participants** - There are tens of thousands of participants - being institutional or retail, each with their own unique set of perspectives, motivations, resources, objectives, strategies, etc.

Multiplying everything together, we can see how many **possible decisions** there are compared to data science - where the company can only choose from a much smaller set of decisions.

## Sources

### First Steps

1. Narang - Conceptual high level overview of quant trading
1. Chan QT - Conceptual high level overview of quant trading 
2. Chan MT - Practical introduction to systematic trading
2. Jansen ML4T - Practical introduction to systematic trading
2. Worldquant AI4T - TBC
3. AEM, APM, QPM  - TBC
