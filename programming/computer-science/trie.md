# Trie

Standard use case is O(1) auto-complete.

Root node has nothing, and then link together full words as children of the preceding
letter. On the last letter of a word, add an `isWord: true` or some sort of signal.

If someone types a letter, lookup all options down the branch of the tree that starts with
the letter they typed [DFS or BFS](./trees.md) and then traverse down the branches
as they type more letters.

You can also score the nodes as users select options so that over time the high score options
can be ordered first.

```
insertion(str) {
    curr = head
    for (c in str) {
        if (curr[c]) {
            curr = curr[c]
        } else {
            node = createNode();
            curr[c] = node;
            curr = node;
        }
    }
    curr.isWord = true;
}
```

For deletion, recursively find the end of a word and then delete your way back up in a post
recursion step.
