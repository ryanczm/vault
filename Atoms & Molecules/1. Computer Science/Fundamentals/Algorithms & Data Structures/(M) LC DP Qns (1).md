Type: #atom
Atom: [[Dynamic Programming Qns (D)]]
Subtopic: Fundamentals
Topic: Computer Science
Status: #inprogress
Understanding: #Exploratory 

----
# Maximum Subarray

Q: Given an integer array `nums`, find the subarray which has the largest sum and return its sum.
A: We can use Kadane's algorithm.

1. Iterate through the range object of the array.
2. (F) `if arr[i-1]>0: arr[i] += arr[i-1]`
3. `return max(arr)

At each iteration, simply add the previous element to the current if the previous element is positive This creates a running sum, as long as the previous element sum is non-negative. This works because subarrays are contiguous. As long as the previous element as the running sum is positive, adding it always results in a larger subarray.
