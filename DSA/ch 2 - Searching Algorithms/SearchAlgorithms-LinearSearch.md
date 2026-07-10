# Searching Algorithms 
-------
# Introduction
Searching is the process of finding a specific element (called the key or target) in a collection of data.
Example :
```txt    
Array = [10, 25, 35, 50, 80]
Target = 35
```
If the target exists, return its position (index). Otherwise, report "Not Found."


# Why Searching is Important?
Slearching is used in almost every software application:
- Login systems (find user by email)
- Contact lists
- Search engines
- File management
- Databases
- Online shopping
- Banking systems

## Types of Searching Algorithms
1> Linear Search
2> Binary Search

## Linear Search
Linear Search checks each element one by one until the target is found or the list ends.

Algorithm:
- Start from the first element.
- Compare it with the target.
- If equal → Found.
- Otherwise, move to the next element.
- Repeat until the end.

Example:
```txt   
Array:

12 25 30 42 55 61

Find 42

12 
25
30 
42 - ✓ Found
```

#### Advantages
- Very simple
- Works on unsorted data
- Easy to implement

### Disadvantages
- Slow for large datasets
- May need to check every element

### Time Complexity

##### Best Case: O(1)
##### Average Case: O(n)
##### Worst Case: O(n)
##### Space Complexity: O(1)