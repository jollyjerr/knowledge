# Heap (priority queue)

A type of [tree](./trees.md) that maintain a weak ordering

Fill in each node from left to right and maintain the heap property (weak ordering to max or min)

### Addition

Add new node to the very bottom and then bubble up (by swapping above) until
the heap property is restored

### Deletion

Remove the node, swap the lowest node in it's place and heapify down

## Min Heap

Top node is the smallest

```
20
|   |
30   100
| |  |  |
31 80 3000 1001
```

## Max Heap

Top node is the largest

## ArrayList Representation

It can be helpful to represent heaps in an array list so accessing elements at the
end is easier.

```
[0, 1, 2, 3, 4, 5, 6, 7, 8]

Children can be found with this function:

2i + 1 === left child
2i + 2 === right child

And a nodes parent can be found with:

Math.floor((i - 1)/2)
```

## Implementation (Min Heap)

```ts
class MinHeap {
	public length: number;
}
```
