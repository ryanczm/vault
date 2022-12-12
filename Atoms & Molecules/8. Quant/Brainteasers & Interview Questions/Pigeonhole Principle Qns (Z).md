Type: #atom
Atom: [[Logic Qns (C)]]
Topic: Quant
Level: #Exploratory 

----
# Overview

These questions use pigeonhole principle. If you have $n$ pigeons and $m$ holes with $n>m$, you need to stuff at least 2 pigeons in one hole to fit all the pigeons. Think of this as an overflowing bucket of water in a discrete fashion.

# Matching Socks Problem 

Q: Drawer contains some red, some yellow and blue socks. Minimum number of socks to guarantee at least one pair of some color?
A: $n+1=3+1=4$, simple application of pigeonhole principle.

# Handshakes

Q: Party with 25 ppl. Each person shakes hands with you. But there are random handshakes with other people too (people don't know each other). Minimum number of handshakes so at least two people shook hands with exactly same number of people?
A: Pigeonhole, so 25+1=26. Assuming no repeated handshakes.

# Have We Met Before? Theorem on Friends & Strangers Question

Q: 6 people at party including you. Show this statement is true: either at least 3 of them are strangers beforehand or at least 3 of them met each other before.
A: This is the [Theorem on Friends & Strangers](https://en.wikipedia.org/wiki/Theorem_on_friends_and_strangers#Proof). To see this, each person is a node. There are 6 nodes in a pentagram. Each dot is connected to other nodes by 5 edges. These 5 edges are of two kinds: known or unknown. Draw out the edges (arrowed edge if known and normal edge if unknown). Then we can see the statement is true. If 3 people know you, then 2 people do not, and if 3 people do not know you, then do people do not.

# Ants on a Square Question

Q: 51 ants on square of length 1. If you have glass of radius 1/7, show you can put your glass to capture at least 3 ants. 
A: This makes no sense to me because ants can climb on top of each other. The proof is that you can divide the square into 25 1/5 length squares. Then assuming the ants are evenly spaced in the square, at least one square must contain 3 points. A circle of radius $r$ can cover a square of side $\sqrt{2}r$ (Pythagoreas' thm). So 1/7 circle can cover a square of side $\sqrt{2}/7 >1/5$ (square both sides to see).

# Counterfeit Coins II Question [!]






