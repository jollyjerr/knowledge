# Graph Traversal

## Shortest Path Problem

If a robot needs to find the optimal path to a target location, it must solve
the shortest path problem.

- **Unweighted graph**

Breadth-First Search can be used to find the shortest path by traversing all
nodes (full traversal).

- **Weighted graph**

Dijkstra's algorithm can be used to find the shortest path between a starting
node and **all** other nodes in a weighted graph.

`A*` (A star) combines the best features of Dijkstra with a greedy heuristic
that guides the robot to the goal node of a weighted graph.

## Complete Traversal

In navigation, the preferred algorithm to completely traverse a graph is
Breadth-First Search. BFS uses a queue, as apposed to DFS which uses a stack,
therefor the **first** path to a target node that is found **will be the
shortest path**.

```py
graph = {
    'A': ['B', 'C'],
    'B': ['A', 'D', 'E'],
    'C': ['A', 'F'],
    'D': ['B'],
    'E': ['B', 'F'],
    'F': ['C', 'E']
}

start = 'A'
goal = 'F'

queue = [start]
visited = set(start)
parent = {}

while queue:
    v = queue.pop(0)
    for u in graph[v]:
        if u not in visited:
            queue.append(u)
            visited.add(u)
            parent[u] = v

key = goal
path = []
while key in parent.keys():
    key = parent[key]
    path.insert(0, key)
path.append(goal)

print(f'Shortest path from {start} to {goal}: ', path)
```
