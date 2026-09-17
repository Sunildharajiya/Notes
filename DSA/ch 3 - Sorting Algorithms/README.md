# Chapter 3: Sorting Algorithms

Sorting means arranging data in a required order, usually ascending or descending. Sorted data is easier to search, compare, and process.

## Why sorting matters

- Makes binary search possible when data is ordered.
- Helps produce readable reports and rankings.
- Simplifies duplicate detection and merging.
- Is used in databases, operating systems, and data analysis.

## 1. Bubble Sort

Bubble sort repeatedly compares adjacent elements and swaps them when they are in the wrong order. After each pass, the largest remaining element moves to the end.

```text
for i = 0 to n - 2
    swapped = false
    for j = 0 to n - i - 2
        if array[j] > array[j + 1]
            swap(array[j], array[j + 1])
            swapped = true
    if swapped == false
        break
```

- Best case: `O(n)` when the array is already sorted and an early-exit check is used
- Average/worst case: `O(n²)`
- Space: `O(1)`
- Stable: Yes

Bubble sort is simple and useful for learning, but it is usually not suitable for large inputs.

## 2. Selection Sort

Selection sort finds the smallest item in the unsorted portion and places it at the next position.

- Best, average, and worst case: `O(n²)`
- Space: `O(1)`
- Stable: Usually no
- Advantage: Performs at most `n - 1` swaps

## 3. Insertion Sort

Insertion sort grows a sorted section one element at a time. It is efficient for small or nearly sorted arrays.

```text
for i = 1 to n - 1
    key = array[i]
    j = i - 1
    while j >= 0 and array[j] > key
        array[j + 1] = array[j]
        j = j - 1
    array[j + 1] = key
```

- Best case: `O(n)`
- Average/worst case: `O(n²)`
- Space: `O(1)`
- Stable: Yes

## 4. Merge Sort

Merge sort divides the array into halves, sorts each half recursively, and merges the sorted halves.

- Best, average, and worst case: `O(n log n)`
- Space: `O(n)` for the temporary arrays
- Stable: Yes

## 5. Quick Sort

Quick sort chooses a pivot, partitions values around it, and recursively sorts both partitions.

- Average case: `O(n log n)`
- Worst case: `O(n²)` with poor pivot choices
- Average space: `O(log n)` for recursion
- Stable: Usually no

## Choosing a sorting algorithm

| Situation | Good choice |
| --- | --- |
| Very small or nearly sorted data | Insertion sort |
| Need a simple educational algorithm | Bubble or selection sort |
| Guaranteed `O(n log n)` time | Merge sort |
| General in-memory sorting | Quick sort or a library sort |

Always check the language's standard library before implementing sorting in production.
