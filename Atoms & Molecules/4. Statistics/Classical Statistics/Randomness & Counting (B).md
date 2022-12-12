Type: #atom
Atom: [[Probability & Counting (B)]]
Subtopic: Classical Statistics
Topic: Statistics
Understanding: #Exploratory Intuition

----
# Overview - What is Randomness (Set of Events)

**Randomness (set of events, event space, sample space)** is a framework for understanding uncertain events. The idea is that if we know the set of all possible outcomes, we can package them an event space. Each element in this set has a probability. 

An **event** is a **grouping of multiple outcomes together** and assigning that a probability. An **experiment** generates the **outcomes**. E.g a outcome is a d6 pip. The experiment is a d6 roll. An event is a d6 pip is odd.

The **naive definition of probability** as defined by Blitzstein is to count the number of outcomes in that event over the total number of outcomes (if each outcome has equal probability). 

# Types of Randomness

Binary - Yes or no - Will it rain tomorrow?
Discrete - A die roll results in one of a finite list of possible outcomes.
Continuous - Tomorrow's temperature could be anything.

# Multiplication Rule

The multiplication rule is a way to enumerate through the number of possible outcomes for a compound experiment (a series of experiments). 

**Using the Multiplication Rule to Construct Outcome Spaces**

**Rectangle**- The canonical randomness visual. Suited for continuous (e.g can draw a squiggly circle).
**Contingency Table** - A 2x2 or 3x3 table. Suited for discrete (e.g dice) but works only up to 3D. 
**List/Tree** - Flatten out the outcomes. Suited for discrete. Each element of the list consists of a tuple of outcomes from each experiment. Use multiplication rule to expand out. A list is a flattened tree.

When we construct a table or list or tree, we are invoking the **multiplication rule** of various experiments. 
Sampling without replacement in the multiplication rule like 10 x 9 x 8 is another case. 

# Independence

If two outcomes are unrelated, we can multiply their probabilities to get the joint of the compound experiment. This is NOT the multiplication rule (which deals with enumerating outcomes)! This is a handy technique to avoid enumeration if two outcomes are independent.

# Complement

Using the complement is another technique where the original problem has too many possibilities to enumerate. To use it, simply flip the problem, calculate the complement, then subtract it off 1 to get the answer. Recognizing use of this technique requires **realizing the number of possibilities is too large for the non-complement** (e.g 99% vs 1%).

An example is the birthday problem - What is probability at least 2 people share same birthday? At least 2 means anywhere from 2-363 people, so the complement is no two people share the same birthday. 

# Random Variables & Expected Value (EV)

Extending the enumeration of an experiment (e.g a card draw), realize that dice roll is a uniform distribution. Not all distributions are uniform. 

If we can assign probabilities to outcomes via a random variable of an experiment, then the expected value is the most important summary statistic.

