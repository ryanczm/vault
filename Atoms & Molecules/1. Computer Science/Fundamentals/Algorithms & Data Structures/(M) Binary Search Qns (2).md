Type: #atom 
Atom: [[Array Qns (D)]]
Subtopic: Fundamentals
Topic: Computer Science
Status: #inprogress 
Understanding: #Exploratory 

----
# Binary Search on Sorted Array 

Q: Perform binary search on a sorted array for element `k` and return it's index `i`.

1. Initialize left and right pointers `l, r = 0, len(arr) - 1`. These are integer indexes. Then `while l <= r:`
2. (W) Calculate the middle index `m = (l+r)//2`. 
3. (W) If `arr[m] < k: l = mid + 1` . If `elif arr[m] > k: r = mid - 1`. Else `else: return mid`. 
4. Exit the loop and return `-1`.

Eventually `l` and `r` converge to 3 elements in the array: `l,m,r` where `m==k`.

# Binary Search on Rotated Array

Q: Search on a sorted array which is rotated.
A: There is a pivot index in which the array is rotated (the two subsets are swapped). We need to use a modified version of binary search that is depend if the array is **left-rotated** or **right-rotated** (if pivot index is left or right of middle index).

1. Initialize left and right.
2. Enter the main body of the while loop.
3. (W) Calculate mid and check if the mid is the target.
4. (W) If it is left rotated (`a[l] < a[m]`) check if `a[l] <= k <= a[m]`. if so, set high to the left neighbour of mid. Else, set low to the right neighbour of mid (normal b.s)
5. (W) Else, it is right rotated. Check if `a[m] <= k <=a[h]`. If so, set low to right neighbour of mid. Else, set high to left neighbour of mid.
