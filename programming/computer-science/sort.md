# Sort

> Any xi in an array is <= xi + 1

## Bubble Sort

Start at the beginning of an array. Each element looks to it's right and swaps if the property of sorted-ness is broken (xi > xi + 1)

Each iteration will put the biggest remaining element at the end of the array. So each iteration can go over N - iteration_count items

Stop iterating when you are only checking an array of one item

Runtime is O(N^2) reduced from `O(n(n+1)/2)`

```ts
function bubbleSort(arr: number[]): void {
	for (let i = 0; i < arr.length; i++) {
		for (let j = 0; j < arr.length - 1 - i; j++) {
			if (arr[j] > arr[j + 1]) {
				const tmp = arr[j];
				arr[j] = arr[j + 1];
				arr[j + 1] = tmp;
			}
		}
	}
}
```

## Quicksort

Quicksort takes advantage of [recursion](./recursion).


