**P1** `Find the Bth smallest element in given array A.`
> NOTE: Users should try to solve it in <= B swaps.

```py
class Solution:
	# @param A : tuple of integers
	# @param B : integer
	# @return an integer
	def kthsmallest(self, A, B):
        l = len(A)
        for i in range(B):
            A = self.find_smallest(A[:l-i])
        return A[-1]
    
    def find_smallest(self,arr):
        arr = list(arr)
        smallest = arr[0]
        index = 0
        l = len(arr)
        for i in range(len(arr)):
            if arr[i] < smallest:
                smallest = arr[i]
                index = i
        # arr = self.swapPositions(arr, index, l-1)
        arr[index], arr[l-1] = arr[l-1], arr[index]
        return arr
```
---

**P2** `Given an array of integers A and an integer B, find and return the difference of B'th max element and B'th min element of the array A.`

```python
def solve(self, A, B):
    A.sort() 
    return A[-B] - A[B-1]
```

---

**P3**: `Given an array of integers A, sort the array into a wave like array and return it, In other words, arrange the elements into a sequence such that a1 >= a2 <= a3 >= a4 <= a5.....`
> NOTE : If there are multiple answers possible, return the one that's lexicographically smallest.

```py
def wave(A):
	    A.sort()
	    x = len(A)
	    i = 0
        while i < x-1:
            A[i], A[i+1] = A[i+1], A[i]
            i = i+2
        return A
```

---

**P4** `Given an array of integers A, find and return new integer array B. Array B has the property where B[i] is the number of smaller elements to the right of A[i].`

```python
A = [ 64, 150, 31, 249, 328, 125, 365, 353, 84, 204, 118 ]

class Node:
    def __init__(self, val):
        self.val = val
        self.left = self.right = None
        self.elemcount = 1
        self.lcount = 0

class Tree:
    def __init__(self, root):
        self.root = root

    def insert(self, node):
        curr = self.root
        cnt = 0 # number of nodes smaller than current

        while curr != None:
            prev = curr
            if node.val > curr.val:
                cnt += curr.elemcount + curr.lcount
                curr = curr.right
            elif node.val < curr.val:
                curr.lcount += 1
                curr = curr.left
            else:
                prev = curr
                prev.elemcount += 1
                break # we dont have to insert a node with same value as current because it is already present
        if prev.val > node.val:
            prev.left = node
        elif prev.val < node.val:
            prev.right = node
        else:
            return cnt + prev.lcount
        return cnt

def solve(A):
    n = len(A)
    B = [0]
    t = Tree(Node(A[-1]))
    for i in range(n-2, -1, -1):
        B.append(t.insert(Node(A[i])))
    return B[::-1]


print(solve(A)) # [1, 4, 0, 4, 4, 2, 4, 3, 0, 1, 0]
```