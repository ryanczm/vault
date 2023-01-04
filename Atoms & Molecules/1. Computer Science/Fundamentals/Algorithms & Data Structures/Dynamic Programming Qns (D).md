Type: #keyatom
Atom: [[Recursion & DP Qns (D)]]
Subtopic: Fundamentals
Topic: Computer Science

----
# Overview

DP is just **recursion** and **memoization**. The recursion is the magic sauce that generates a series of calls. It is constructed carefully to solve the problem by generating a series of calls that covers all parts of the problem. 

At each step, the call can modify some states which can be stored (memoized), or use an existing state (lookup existing states) to save on computation.

We need a strong foundation of **recursion**.

# Structure

**Data Structure** - Set up the structure for the recursion to operate on (e.g some graph)
**Memoizations** - Set up the memoization structures. These will be modified and used by recursive calls. Often, the recursion function is decorated with some caching decorator that tells the interpreter to store the result of the call instead of recomputing.
**Recursion** - The heart of hte problem - the recursive code that will solve the problem.