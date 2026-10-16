# Q1. Complexity Analysis of Searching and Sorting Algorithms

## 1. Bubble Sort

Bubble sort repeatedly compares adjacent elements and swaps them if they are in the wrong order.

### Time Complexity

- **Best Case:** `O(n)` — When the array is already sorted and an early-stop optimization is used.
- **Average Case:** `O(n²)` — When the array is randomly ordered.
- **Worst Case:** `O(n²)` — When the array is sorted in reverse order.

### Space Complexity

- **Iterative Approach:** `O(1)` because only a few extra variables are required.
- **Recursive Approach:** `O(n)` recursion stack space.

### Stability and In-place

- **Stable:** Yes. Adjacent elements are swapped only when they are strictly out of order, so equal elements retain their relative order.
- **In-place:** Yes. The algorithm rearranges elements in the original array using constant extra space.

## 2. Insertion Sort

Insertion sort builds a sorted portion of the array by inserting each element into its correct position.

### Time Complexity

- **Best Case:** `O(n)` — When the array is already sorted.
- **Average Case:** `O(n²)` — When the array is randomly ordered.
- **Worst Case:** `O(n²)` — When the array is sorted in reverse order.

### Space Complexity

- **Iterative Approach:** `O(1)` because no additional array is required.
- **Recursive Approach:** `O(n)` recursion stack space.

### Stability and In-place

- **Stable:** Yes. The algorithm shifts only elements greater than the current element, preserving the relative order of equal elements.
- **In-place:** Yes. Elements are shifted within the original array using constant extra space.

## 3. Selection Sort

Selection sort repeatedly finds the minimum element in the unsorted portion and swaps it with the first element of that portion.

### Time Complexity

- **Best Case:** `O(n²)` — Even when the array is already sorted, the algorithm scans the remaining unsorted elements to find the minimum.
- **Average Case:** `O(n²)` — When the array is randomly ordered.
- **Worst Case:** `O(n²)` — When the array is sorted in reverse order.

### Space Complexity

- **Iterative Approach:** `O(1)` because only a few extra variables are required.
- **Recursive Approach:** `O(n)` recursion stack space.

### Stability and In-place

- **Stable:** No. Swapping the minimum element with the first element of the unsorted portion can change the relative order of equal elements.
- **In-place:** Yes. The algorithm swaps elements within the original array using constant extra space.

## 4. Merge Sort

Merge sort divides the array into smaller halves, recursively sorts them, and merges the sorted halves.

### Time Complexity

- **Best Case:** `O(n log n)` — Regardless of the initial order, the standard implementation divides and merges the array.
- **Average Case:** `O(n log n)` — When the array is randomly ordered.
- **Worst Case:** `O(n log n)` — Even when the array is sorted in reverse order.

### Space Complexity

- **Auxiliary Array:** `O(n)` for storing elements during merging.
- **Recursion Stack:** `O(log n)` because the array is repeatedly divided into halves.
- **Total Auxiliary Space:** `O(n)`.

### Stability and In-place

- **Stable:** Yes. During merging, if two elements are equal, the element from the left half is chosen first, preserving their relative order.
- **In-place:** No, in the standard array implementation, because an additional array of size `n` is used for merging.

## 5. Quick Sort

Quick sort selects a pivot, partitions the array around it, and recursively sorts the resulting partitions.

### Time Complexity

- **Best Case:** `O(n log n)` — When each pivot divides the array into approximately equal parts.
- **Average Case:** `O(n log n)` — When partitions are reasonably balanced on average.
- **Worst Case:** `O(n²)` — When partitions are repeatedly highly unbalanced, such as sizes `0` and `n-1`.

### Space Complexity

- **Best/Average Case:** `O(log n)` recursion stack space when partitions are balanced.
- **Worst Case:** `O(n)` recursion stack space when partitions are repeatedly unbalanced.

### Stability and In-place

- **Stable:** No. Swapping elements during partitioning can change the relative order of equal elements.
- **In-place:** Yes, for the standard in-place partitioning implementation, because elements are rearranged within the original array. However, the recursion stack requires additional memory.

### Big-O, Big-Omega and Big-Theta

- **Big-O (`O`):** Represents an asymptotic upper bound.
- **Big-Omega (`Ω`):** Represents an asymptotic lower bound.
- **Big-Theta (`Θ`):** Represents a tight asymptotic bound when the upper and lower bounds match.

For Quick Sort:

- **Best Case:** `Θ(n log n)` — Partitions are balanced.
- **Average Case:** `Θ(n log n)` — Partitions are reasonably balanced on average.
- **Worst Case:** `Θ(n²)` — Partitions are repeatedly highly unbalanced.

Therefore, the worst-case running time is `O(n²)`, and the worst-case lower bound is `Ω(n²)`, giving a worst-case running time of `Θ(n²)`.

## 6. Linear Search

Linear search checks each element sequentially until the target is found or the array ends. The array does not need to be sorted.

### Time Complexity

- **Best Case:** `O(1)` — When the target is the first element.
- **Average Case:** `O(n)` — When the target is typically found after examining a linear number of elements.
- **Worst Case:** `O(n)` — When the target is the last element or is absent.

### Space Complexity

- **Iterative Approach:** `O(1)` because only a few variables are required.

### In-place

- **In-place:** Yes. The algorithm searches the original array without requiring additional data structures.

**Stability:** Stability is not applicable because linear search is a searching algorithm, not a sorting algorithm.

## 7. Binary Search

Binary search repeatedly halves the search interval to find a target in a sorted array.

### Time Complexity

- **Best Case:** `O(1)` — When the target is the middle element.
- **Average Case:** `O(log n)` — When several halvings are required to find the target.
- **Worst Case:** `O(log n)` — When the target is absent or requires the maximum number of halvings to locate.

### Space Complexity

- **Iterative Approach:** `O(1)` because only a few variables are required.
- **Recursive Approach:** `O(log n)` because recursive calls require stack space.

### In-place

- **In-place:** Yes, for the standard iterative implementation, because it searches the original sorted array using constant extra space.

**Stability:** Stability is not applicable because binary search is a searching algorithm, not a sorting algorithm.

## 8. Summary Table

| Algorithm | Best Time | Average Time | Worst Time | Auxiliary Space | Stable? | In-place? |
|---|---|---|---|---|---|---|
| Bubble Sort | `O(n)` | `O(n²)` | `O(n²)` | `O(1)` iterative | Yes | Yes |
| Insertion Sort | `O(n)` | `O(n²)` | `O(n²)` | `O(1)` iterative | Yes | Yes |
| Selection Sort | `O(n²)` | `O(n²)` | `O(n²)` | `O(1)` iterative | No | Yes |
| Merge Sort | `O(n log n)` | `O(n log n)` | `O(n log n)` | `O(n)` | Yes | No |
| Quick Sort | `O(n log n)` | `O(n log n)` | `O(n²)` | `O(log n)` average; `O(n)` worst | No | Yes |
| Linear Search | `O(1)` | `O(n)` | `O(n)` | `O(1)` iterative | N/A | Yes |
| Binary Search | `O(1)` | `O(log n)` | `O(log n)` | `O(1)` iterative | N/A | Yes |

## Conclusion

Bubble sort and insertion sort perform well on already sorted inputs. Selection sort performs quadratic work regardless of input order. Merge sort guarantees `O(n log n)` time but requires additional array space. Quick sort is efficient on average but can take `O(n²)` time in the worst case. Linear search works on unsorted arrays, whereas binary search requires a sorted array and can locate elements in logarithmic time.
