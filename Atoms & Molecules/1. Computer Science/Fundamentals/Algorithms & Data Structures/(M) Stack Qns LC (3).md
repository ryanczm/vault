Type: #atom 
Atom: [[Stack Qns (D)]]
Subtopic: Fundamentals
Topic: Computer Science
Status: #inprogress
Understanding: #Exploratory 

----
# Evaluate Reverse Polish Notation

Q: Given an array of strings `tokens` that represents an arithmetic expression in [RPN](https://en.wikipedia.org/wiki/Reverse_Polish_notation), evaluate the expression. [Solution](https://leetcode.com/problems/evaluate-reverse-polish-notation/solutions/47444/python-easy-to-understand-solution/?orderBy=most_votes)
A: We can use a stack. Simply iterate through each token, adding it to the stack if it is a digit (not an operator). If it isn't, we pop the last two values off the stack and evaluate the expression, then add it back to the stack via append. Once the loop is over, we pop the stack (topmost value) for our answer.

# Min Stack

Q: Implement a stack that supports pop, push, peek and **min** (retrieve min element) operations in  constant time.
A: At each append in the stack, simply compare the incoming value with the minimum. So we need two stacks  (one for values, one for the minimum at each position). Each time we push on the stack, we need to push the minimum value so far onto the minstack. Each time we pop, we pop the minstack. Then getmin is simply popping the minstack.

# Daily Temperatures 

Q: Given an array of integers, return an array where the ith element is the number of days you have to wait after the ith day to get a warmer temperature (higher integer). If there isn't, then it is 0. [Solution](https://www.youtube.com/watch?v=cTBiBSnjO3c&ab_channel=NeetCode). 
A: We can use a monotonic stack. We create an array of 0s and an empty stack. Iterating through our temperatures, while the current temperature is greater than the top of the stack, we pop and assign the number of days of this difference at the popped stack index at the result. Then, we append stack. Then, we exit the for loop, and return the result.

