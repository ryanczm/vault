Type: #atom
Atom: [[Markov Chains (J)]]
Subtopic: Classical Statistics
Topic: Statistics
Status: #inprogress 
Understanding: #Exploratory 

----
# Overview

Gambler's ruin is a game that can be modelled with a Markov chain with absorbing states.

Essentially, two players play a game with **their own amounts of money/points (the state)**, and the loser hands to the winner **some quantity each round** (thus transiting to the next state and **defining state space**). Each party has **unequal probability of winning** (transition probability/matrix) each round. 

The overall winner is declared once one person runs out of money (the absorption states).

Often it is modelled in a David Goliath setup where one party has a higher skill, but the other party has a higher starting quantity. 

There is a special formula for absorption probabilities.

