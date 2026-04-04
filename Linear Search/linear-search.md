# LINEAR SEARCH IN D.S.A.
## What is Linear Search?
- Linear Search is the simplest searching algorithm.
- It checks each element one by one until the target element is found or the list ends.

- Works on: Arrays, Lists,Unsorted data

## How it Works
1. Start from the first element
2. Compare it with the target
3. If match → return index
4. Else → move to next element
5. Repeat until end

## Example
Array: [10, 25, 30, 45, 50]
Target: 30
Steps:
Compare 10 ❌
Compare 25 ❌
Compare 30 ✅ (Found at index 2)

### Steps
```txt
for i from 0 to n-1:
    if arr[i] == target:
        return i
return n-1
```

## Javascript
```js
function linearSearch(arr, target) {
    for (let i = 0; i < arr.length; i++) {
        if (arr[i] === target) {
            return i; // found
        }
    }
    return -1; // not found
}

// Example
console.log(linearSearch([10, 25, 30, 45], 30)); // 2

```

## Time Complexity
- Best Case: O(1) → element found at first position
- Worst Case: O(n) → element at last or not found
- Average Case: O(n)

### Space Complexity
O(1) (no extra space used)

### Advantages
- Simple to understand
- Works on unsorted data
- No preprocessing required

### Disadvantages
- Slow for large datasets
- Not efficient compared to Binary Search

### When to Use?
- Small datasets
- Unsorted arrays
- When simplicity is important

## better approach
If array is unsorted → use Linear Search
If array is sorted → prefer Binary Search