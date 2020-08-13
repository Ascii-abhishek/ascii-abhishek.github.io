# Sorting Techniques

---

**P1**: `Given an unteger array, find kth largest element, given that you cant use extra memory`
>- one way could be findint the largest element in the array and swap it with the last element of the array
>- then reduce the array upto second last elemnt and repeat this above and this step k times
>- at last we would have kth largest element in the remaining array as last element of it.
>- In one operation we are traversing N elements and we are doing this operations k times, So, time complexity => O(kN)
>- and if we perform the same operation N times then we would have sorted array with time complexity => O(N<sup>2</sup>).
>- this method of sorting is known as `Selection Sort`.

>- If we traverse following way:
>   - we can swap only adjecent elements i.e. if A[i] > A[i+1], A[i] <==> A[i+1]
>   - here also we have to perform k operations where each operation is to parse N elements to get kth largest element.
>   - And if we continue operations for N-1 times, we would have sorted array at last. and time complexity would be O(N<sup>2</sup>).
>   - This sorting technique is known as `Bubble sort` Algorithm.
> - Cost wise `Selection sort` is less costly as there are atmost one swap, whereas there are atmost n-1 swaps in `Bubble sort`.

**P2**: `During a card game, dealer can distribute only one card at a time, problem is to sort cards which you have continuously as you receive one`
>- here you place first card at first position.
>- then as you keep on receiving cards, you find a correct position, move other cards if you have to to make space and then put current card at its correct position.
>- Here in first opration:
>   - we have to find a correct place for the element, linear search would be O(N), but here the previous cards would be already sorted so we can use binary search which is of O(logN).
>   - once we find the position, we move atmost N cards to the right, taking O(N)
>- So one operation costs o(logN + N) => O(N).
>- And to complete sort we have to perform N operations, thus making total time complexity of order O(N<sup>2</sup>)
>- THis type of sorting technique is known as `Insertion Sort`

**P3**: `Given an array where all odds and even elements are sorted, we are required to sort the whole array`
> 3, 9, 2, 4, 25, 10, 19
>- we can make two separate arrays, one containing all odd elements and other containing all the even elements.
>- then using two pointers approach, placing one pointer at start of odd array and other at start of even array, let say i, j
>- if Odd[i] < Even[j], select Odd[i] and i++, else select Even[j]++.
>- keep on placing selected elements in a separate array and at last, we will have sorted array
>- here diving array into two is of O(N, then selecting smaller elements would take O(N), thus total complexity would be O(N+N) => O(N).
>- this solution is conquer part of the divide and conquer solution approach
>- Solution where we divide an array into parts, sort them, and then merge is known as `Merge Sort`.
>- we keep on dividing the array into two parts > O(logN) and sorting, So, time complexity of merge sort is O(NlogN).
>- Space complexity would be O(N)

**P4**: `Inversion Count. inversion means there present i, j where i < j and A[i] < A[j], we need to count total number of such inversions in array`
> 4, 5, 1, 2, 6, 3
>- here inversion present at indexes: (0, 2), (0, 3), (0, 5), (1, 2), (1, 3), (1, 5), (4, 5) ==> total of 7 inversions