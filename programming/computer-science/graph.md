# Graph

A collection of nodes with some amount of directed or non-directed connections.

cycle: three or more nodes linked together in a loop

connected: every node can reach every other node

directed: one way connections between nodes

weight: the cost of a link between nodes

dag: directed acyclic graph

node === vertex

## Representation

Normally represented with:

### Adjacency List

Stored in a 2d array. An index is a node and the array at that index is a list of edges.

```ts
[
	[
		{ to: 3, weight: 10 },
		{ to: 5, weight: 4 }
	],
	[{ to: 1, weight: 1 }]
];
```

### Adjacency Matrix (O(V^2))

Like an adjacency list but each subarray shows the weight of connections to all other nodes. No
connection is represented with a 0.

```ts
[
	[0, 0, 10, 0, 4],
	[0, 1, 0, 0, 0]
];
```

## Search

All [trees](./trees.md) are graphs, so just use DFS or BFS.

```ts
function bfs(graph: WeightedAdjacencyMatrix, source: number, needle: number): number[] | null {}
```
