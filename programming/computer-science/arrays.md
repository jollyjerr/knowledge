# Arrays

An array is a contiguous memory space that contains a certain amount of bytes.

```
a = int[3]

a[1] <- go to memory address of a and add how big my type is * the index (in this case 4 bytes (32 bit int) * 1)
```

- Insertion just overwrites a + width \* offset (O(1))

- Deletion depends on the system, just insert "not something"

- Cannot grow traditional arrays

- No Array.size() in most basic implementation - you need to have 1. a pointer to the start of the array 2. the size of the things in the array 3. the number of things in the array

> TIP: In JS, use an ArrayBuffer to replicate true arrays.
