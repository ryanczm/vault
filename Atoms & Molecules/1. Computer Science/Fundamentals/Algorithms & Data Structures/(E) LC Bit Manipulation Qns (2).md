Type: #atom 
Atom: [[Bit Manipulation Qns (D)]]
Subtopic: Fundamentals
Topic: Computer Science
Status: #inprogress 
Understanding: #Exploratory 

----
# Lonely Integer (Bit Manipulation)

Q: Given an array of integers, where all elements except one appear twice, find the lonely integer.
A: This is a bit manipulation question. We simply need to set a variable to 0, then loop through the array, doing a bitwise XOR assignment between that variable and the iterable: `for i in range(n): x ^= a[i]`. For each bit field, the paired numbers cancel, leaving the singleton number's bit behind - [Solution](https://www.hackerrank.com/rest/contests/master/challenges/three-month-preparation-kit-lonely-integer/hackers/brangaswamy2018/download_solution)


# Flipping Bits (Bit Manipulation)

Q: Given a 32-bit unsigned integer, write code to flip the bits.
A: We can use the bitwise negation operator `~n` in Python, but because this flips the sign bit, we have to add `2**32` to the result. 

