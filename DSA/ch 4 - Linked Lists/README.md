# Chapter 4: Linked Lists

A linked list is a linear data structure made of nodes. Each node stores a value and a reference to another node.

```text
head -> [10 | next] -> [20 | next] -> [30 | null]
```

Unlike an array, linked-list nodes do not need to be stored next to one another in memory.

## Node structure

```text
Node:
    data
    next
```

The `head` points to the first node. An empty list has `head = null`.

## Common operations

### Traversal

Start at `head` and follow `next` until `null`.

```text
current = head
while current != null
    visit current.data
    current = current.next
```

### Insert at the beginning

```text
newNode.next = head
head = newNode
```

This operation takes `O(1)` time.

### Search

Compare each node's value while traversing the list. Search takes `O(n)` time because random access is not available.

### Delete a node

Keep track of the previous node. When the target is found, connect the previous node directly to the target's next node.

## Types of linked lists

1. **Singly linked list:** each node points to the next node.
2. **Doubly linked list:** each node points to both the previous and next nodes.
3. **Circular linked list:** the final node points back to the first node.

## Complexity

| Operation | Singly linked list |
| --- | --- |
| Access by index | `O(n)` |
| Search | `O(n)` |
| Insert at head | `O(1)` |
| Delete at head | `O(1)` |
| Insert after a known node | `O(1)` |

## Advantages and disadvantages

### Advantages

- Dynamic size
- Fast insertion and deletion when the position/node is known
- Does not require contiguous memory

### Disadvantages

- Extra memory is required for references
- No direct indexing like `array[i]`
- Traversal is usually slower because of poor cache locality

Linked lists are useful for implementing stacks, queues, browser history, and adjacency lists in graphs.
