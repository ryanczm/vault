Type: #atom
Atom: [[Backtesting]]
Topic: Quant 
Status: #incomplete 
Understanding: #Exploratory 

----
# Overview

There are two kinds of implementation paradigms of backtesting, **vectorized** vs **event-driven (stream-based)**. These are similar to software design or programming paradigms (e.g how to design something). 

# Vectorized Backtesting

Feed in a signal vector (position vector) and multiply by the forward returns vector to evaluate the **equity curve (?)**.

# Event-Driven Backtesting

Apparently, this is a more detailed, complicated paradigm that avoids lookahead bias and is more realistic (e.g transaction costs, etc). It feeds in events and simulates the strategy.

The main difference is that **vectorized backtesting** is a **moniker for a quick and simple strategy test** whereas **event-driven backtesting** is the **actual proper setup**.

