# LINEAR SEARCH PROBLEM 1

### PROBLEM: Search 7 in this array

use this array to solve this problem [4, 8, 1, 7, 3]

#### Expected ans is 3 


```js
// Define the array and target value

let arr = [4, 8, 1, 7, 3];
let target = 7;

// Initialize index to -1, assuming target is not found
let index = -1;

// Iterate through the array to find the target
for (let i = 0; i < arr.length; i++) {
  if (arr[i] === target) {
    // Update index and break the loop if target is found
    index = i;
    break;
  }
}

// Log the result
if (index !== -1) {
  console.log(`Target is at index ${index}`);
} else {
  console.log('Not found');
}
```

## Code Breakdown
- Initialize an array `arr` with elements and a `target` variable with the value to be searched.
- Initialize an `index` variable to -1, assuming the target is not found initially.
- Iterate through the array using a for loop, checking each element for a match with the target.
- If a match is found, update the `index` and break the loop.
- After the loop, check if the `index` is still -1. If it is, the target was not found; otherwise, log the index of the target.
