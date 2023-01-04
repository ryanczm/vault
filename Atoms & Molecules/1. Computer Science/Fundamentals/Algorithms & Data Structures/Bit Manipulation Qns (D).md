Type: #keyatom  
Atom: [[Bit-Based Qns (D)]]
Subtopic: Fundamentals
Topic: Computer Science

----
# Overview

Bitwise operators perform bitwise operations on **integers** - or the binary representation of integers, it performs the bit manipulation, and returns the new integer. Integers are 32 bits (4 bytes) in Python. The key is to completely disregard integer values and visualize the underlying bit array of the integer.

Start from **rightmost bit** and **zero index** - (3,2,1,0).

# Logic

We have bitwise AND: `x & y` , bitwise OR: `x | y`, bitwise XOR: `x ^ y`, bitwise NOT `~x`,

# Shifting

We have leftwise bitshift `a << n` which shifts the bits of `a` by `n` places. It fills the new right space with `0`. We also have rightwise bitshift `a >> n`, and floors the result (rightwise bitshift is equivalent to halving it). Notice the target array is always on the left hand side. **Bitshifting broadcasts shape leftwards**: if we bitshift a 1 by 2 to the left, the new array is `100`. If we compare `1000` to `10`, the latter broadcasts left to `0010`.

# Individual Bit Operations

These involve left bitshifting to get an array of 0s except for 1 at the desired index like `00010000` then performing some logical operation.

Check Set - Bitshift to index then AND: `mask & (1 << 5)`
**Set** - We bitshift to the desired index then OR it: `mask | (1 << 5)`.
**Unset** - Bitshift to index, negate and AND: - `mask & ~(1 << 5)`
**Toggle** - Bitshift to index, XOR: `mask ^ (1 << 5)`. This goes on > off > on > ...
Array of 1's - `(1 << n) - 1` 