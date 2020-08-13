# Two Pointers

---

>**P1:** `Given a sorted array, arr and an integer k, find a pair [i, j] where arr[i] + arr[j] = k`
>
>- Brute force would be two looks and check for every i and j. O(N<sup>2</sup>).
>- Or, for every we can search for j where A[j] = k - A[i], here searching can be via binary search i.e. O(log(N)) and for N i, total complexity can be O(N.Log(N)).

## Two Pointers concept

- Pointer is just a variable pointing to any index of the array.
- We only have to consider two problems in pointers approach:
  - Where to place both
  - How to update both
- This concept mostly works for sorted arrays
- So in above problem, let's first put both pointers at each end of array
  - A[i] + A[j] == k , return i, j
  - A[i] + A[j] < k, then we only have to push left side (i) pointer to right, because only that will increase sum value
  - A[i] + A[j] > k, then we only have to push right side (j) pointer to left
  - Stopping condition in while loop would be when j <= i, because after this we are just checking with same values again.

>**P2:** `Given a sorted array, arr and an integer k, find a pair [i, j] where arr[j] - arr[i] = k`
>
>- Let's first put both pointers at each end of array
>  - A[j] - A[i] == k , return i, j
>  - A[j] - A[i] < k, but in this case i++ and j-- both will more decrease the diffrence
>- So, we should put i at 0 and j at 1
>  - A[j] - A[i] == k , return i, j
>  - A[j] - A[i] < k, we can increase j till the length of array
>  - A[j] - A[i] > k, we can increase i till the length of array
>  - loop will run till j reaches the end of array (j == n)
>- With two pointers solution in both of above problem, solution is reduced to O(N)

>**P3:** `Given a sorted array, arr and an integer L, find a triplet [i, j, k] where arr[i] + arr[j] + arr[k] = L`
>- Here the brute force would be simply O(N<sup>3</sup>)
>- If we apply concept like two pointers, for every i, find a pair(j, k) such that  arr[j] + arr[k] = L - arr[i]. this solution would be O(N).O(N) >> O(N<sup>2</sup>, which is way better than brute force)

>**P3:** `Given a sorted array, arr and an integer M, find a quadruple [i, j, k, l] where arr[i] + arr[j] + arr[k] + arr[l]= M`
>- here also we can apply same conept as, for every i, j find k, l. and it will be of O(N<sup>3</sup>)
>- another way could be we can create an array with sum of all possible pair of arr, i.e. for all i, j, B[index] = arr[i] + arr[j], also we can do the same for k and l. So, at last we would have two arrays...................

>**P3:** `Given an unsorted array, find a pair i, j such that sum(arr[i:j+1]) == k`
>- Here we can make a prefix sum array, where value at each index i => sum(arr[:i+1]). And we can say that prefix sum array will be sorted, thus two pointer concept can be applied.
>- prefix sum array changes the problem as to find i, j such that P[j] - P[i] = k.
>- forming a prefix sum requires O(N), and finding i, j is O(N) using two pointers, SO, whole will be of O(N + N) >> O(N).