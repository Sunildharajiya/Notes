# Chapter 5: Stacks and Queues

Stacks and queues are linear data structures that control the order in which items are removed.

## Stack: LIFO

A stack follows **Last In, First Out (LIFO)**. The last item inserted is the first item removed.

```text
push(10)
push(20)
pop()  -> 20
```

### Stack operations

- `push`: add an item to the top
- `pop`: remove and return the top item
- `peek`/`top`: read the top item without removing it
- `isEmpty`: check whether the stack has no items

These operations should take `O(1)` time.

### Stack applications

- Undo and redo functionality
- Browser back history
- Function-call management and recursion
- Checking balanced parentheses
- Depth-first search (DFS)

## Queue: FIFO

A queue follows **First In, First Out (FIFO)**. The first item inserted is the first item removed.

```text
enqueue(10)
enqueue(20)
dequeue()  -> 10
```

### Queue operations

- `enqueue`: add an item at the rear
- `dequeue`: remove an item from the front
- `front`: read the first item
- `isEmpty`: check whether the queue is empty

A queue should use a front index or linked-list pointers so that `dequeue` does not shift every element. With that design, enqueue and dequeue are `O(1)`.

### Queue applications

- Print jobs
- Task scheduling
- Network request handling
- Breadth-first search (BFS)
- Customer service systems

## Circular queue

In an array queue, a circular design reuses spaces released at the beginning. The next position can be calculated with:

```text
next = (index + 1) % capacity
```

This avoids unnecessary shifting and gives predictable performance.

## Stack vs queue

| Feature | Stack | Queue |
| --- | --- | --- |
| Removal order | LIFO | FIFO |
| Add operation | `push` at top | `enqueue` at rear |
| Remove operation | `pop` from top | `dequeue` from front |
| Typical traversal | DFS | BFS |

Choose a stack when the newest item should be handled first. Choose a queue when requests should be handled in arrival order.
