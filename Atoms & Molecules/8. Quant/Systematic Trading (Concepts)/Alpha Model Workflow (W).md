Type: #theorem 
Atom: [[Alpha Models (N)]]
Topic: Quant
Understanding: #Exploratory 

----
The workflow in AI4T made heavy use of Pandas DataFrames comparison operations.

# Alpha Logic - Data to Forecasts/Rules

Input - **Data**
Output - **Forecasts** or **comparison numbers**

The alpha logic phase takes data and produces **comparison numbers** in a `DataFrame`. These can be simple rules. The purpose of these numbers is to be applied to prices in the next phase to generate signals. E.g in the momentum strategy, the comparison was the highest $n$ stocks with highest monthly returns.

# Signal Emission - Applying Rules to Price Data to Generate Signals

Input - **Price/returns**, **comparison numbers**
Output - **Signals**

In the signal emission phase, we apply the comparison numbers to the price DataFrame to generate a **signal DataFrame**, which captures the decision. In code, usually it takes the **comparison numbers** and applies some **comparison operator** to the **prices/returns** generate a **Boolean/Integer-valued array**. Nuances:

* **L/S Separation & Combination** - L/S signals can be generated separately but must be combined together often by `-` operator.
* **Signal Idempotency Filtering** - Removing redundant signals to ensure **signal dempotency within lookahead period** (e.g long an already long stock for $n$ days has no effect)
* **Position Sizing** - From `1`, `-1`,  `0` to position sizes.

# Signal Execution - Applying Signals to Returns (!)

Input - **Signals**
Output - **Signal returns**

In the signal execution phase, we apply the signals to **lookahead returns** via the overloaded `*` operator. This generates our **signal lookahead returns**, generated from **lookahead prices**, which is the prices **shifted one period ahead** by the **lookahead window**. 

The **lookahead window duration** is the **minimal time between any two signals** (e.g in monthly strategy, the minimum time between a decision is a month, hence we shift by a month).

Why can we multiply the signal dataframe directly with the lookahead returns dataframe? What about do-nothing signals with `0`?

# Evaluation/Backtesting

Input - **Signal returns**
Output - **Performance measures & statistics**