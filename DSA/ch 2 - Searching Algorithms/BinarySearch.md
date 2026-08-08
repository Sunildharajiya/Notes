# Binary Search
-----------------
## What is Binary Search?
Binary Search is a searching algorithm used to find a particular value, called the target, inside a sorted data structure such as an array.
Instead of checking every element one by one, Binary Search:
- "Checks the middle element and eliminates half of the remaining search space after every comparison."

Example:
```
Array:
[10, 20, 30, 40, 50, 60, 70]
```
Target = 60
We don't need to check:

10 → 20 → 30 → 40 → 50 → 60

Instead:
```
[10, 20, 30, 40, 50, 60, 70]
             ↑
           middle
```
60 > 40

Therefore, everything before 40 can be ignored.
```
[50, 60, 70]
```
Then we repeat the process.

## Why is Binary Search used?
The main reason is speed.

Consider an array containing:
1,000,000 elements
#### Linear Search
Linear Search may need to check:
``` 
1 → 2 → 3 → 4 → ... → 1,000,000
```
In the worst case, it checks 1,000,000 elements.
#### Binary Search 
approximately does:
```
1,000,000
      ↓
500,000
      ↓
250,000
      ↓
125,000
      ↓
...
      ↓
1
```
It takes only around 20 comparisons to reduce one million possibilities to one.
That's why Binary Search is important in algorithms and computer science.

- The most important condition is:
The data must be sorted in the same order that the algorithm expects.
sorted in 0 to n or n to 0

- The iterative Binary Search algorithm usually uses three variables:
`left`,`right`,`center/mid`

## Complete algorithm
For an ascending sorted array:
```
1. Set left = 0
2. Set right = array.length - 1

3. While left <= right:

      Find middle:
      mid = floor((left + right) / 2)

      If array[mid] == target:
          return mid

      If target > array[mid]:
          left = mid + 1

      If target < array[mid]:
          right = mid - 1

4. If loop ends:
      target does not exist
```

## When should you use Binary Search?
Binary Search is useful when:
- Data is sorted.
- You need to perform many searches.
- The dataset can be large.
- Fast searching is important.
- You can access elements by index efficiently.

## conclution
 Binary Search is not ideal for every data structure. Its classic form works especially well with random-access arrays, where you can quickly access arr[mid].