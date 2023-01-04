Type: #atom 
Atom: [[Linked List Qns (D)]]
Subtopic: Fundamentals
Topic: Computer Science
Status: #inprogress 
Understanding: #Exploratory 

----
# Reversing Linked List

Q: Reverse a singly linked list.
A: The trick involves a triple compound assignment. The `.next` attribute should now be the previous node.

1. Initialize `cur = head` and `prev = None`.
2. Whilte `cur`, initialize `cur.next` to `prev` (current head points to none), `prev` to `cur` and `cur` to `cur.next` like so  `while cur: cur.next, prev, cur = prev, cur, cur.next`.

# Palindrome Linked List

Q: Given a singly linked list and it's `head`, determine if this linked list is a palindrome. 
A: We want to do it in $\mathcal{O}(1)$ space and $\mathcal{O}(N)$ time. [Solution](https://www.youtube.com/watch?v=yOzXms1J6Nk&ab_channel=NeetCode). Tests 3 concepts: tortoise & hare, reversing a linked list.

1. Tortoise & Hare - While loop, advance fast and slow pointers.
2. Reverse second half of linked list - `while slow:` swap slow and next.
3. Iterate from front and back - `while slow:` check if not same, else advance and reassign.