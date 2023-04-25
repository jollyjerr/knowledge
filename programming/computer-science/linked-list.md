# Linked List

A heap allocated set of containerized nodes that point to the next node in the list:

```ts
type Node<T> = {
	item: T;
	next?: Node<T>;
};
```

A _doubly_ linked list includes a pointer to previous:

```ts
type Node<T> = {
	item: T;
	next?: Node<T>;
	previous?: Node<T>;
};
```

Insertion/Deletion can be O(1) (if you know where it is) because you just change `next` and `previous` pointers.
All operations in general can be O(N) because of the traversal but obviously head/tail stuff can be constant.

Here is a general interface of a linked list implementation:

```ts
interface LinkedList<T> {
	get length(): number;
	insertAt(item: T, index: number): void;
	remove(item: T): T | undefined;
	removeAt(index: number): T | undefined;
	append(item: T): void;
	prepend(item: T): void;
	get(index: number): T | undefined;
}
```
