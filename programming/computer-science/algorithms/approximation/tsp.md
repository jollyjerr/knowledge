# Traveling Salesperson Problem

Given an undirected, complete, weighted graph.

Want to know the optimal tour of the graph: start from anywhere and visit all
the vertices exactly once and then end where you started.

Goal: find a tour that minimizes the cost (using edge weights as the cost).

Symmetric TSP is undirected graph, Asymmetric is when edges cost different
amounts depending on the direction.

Applications:

- Logistics (scheduling and delivery)
- Manufacturing (printing circuit boards)
- Robotics (route planning)

## NP Complete and NP Hard

TSP is an NP-Complete problem. All efficient solutions are not precise, and all
precise solutions are not efficient.

You can prove TSP is NP-Complete by reducing from Ham Cycle (which itself
reduces from 3-SAT)

In Ham Cycle you do not have a complete graph and there are no weights involved
and you just ask if a TSP Tour exists on the graph. You reduce by making every
existing edge have a cost of 1 and then adding all the missing edges with a
higher cost. Then ask for a TSP tour with cost `<= n+1`

TSP is NP-Hard because you can prove that any algorithm that could approximate
within a constant factor would inherently solve the Hamiltonian Cycle problem in
polynomial time. Because no such algorithm "can exist", then approximating TSP
to any constant factor is impossible.

```
T = cost of algorithm

Thus if 𝑇≤𝛼𝑛, we know that the optimal tour has to be of size ≤𝛼𝑛. This immediately tells us that
a Hamiltonian cycle must exist in the original graph.

On the other hand if 𝑇>𝛼𝑛 then, we have OPT≥1𝛼𝑇>𝑛.
However, OPT>𝑛 tells us that no Hamiltonian cycle may exist in the original graph.

Therefore, even though the approximation algorithm does not compute an optimal tour, its
approximation guarantees are sufficient for us to resolve whether or not the graph has a Hamiltonian cycle
by simply checking if the approximation algorithm finds tour of cost ≤𝛼𝑛 or not.
```

Only generic TCP is NP-Hard.

If your TCP is metric or uclydian you start to be able to prove approximation
algorithms.

## Exact Algorithms

For symmetric TSPs.

### Brute Force

Think of all permutations of `1,2,...,n` vertices (count of n!). Regard each permutation as a
tour and then tour them.

```
O(n*(n!))
```

### Held and Karp

Dynamic programming approach.

```
O(n^2*2^n)
```

Start at a node and go to some subset of vertices, then to e (endpoint), and
then back to 1. The decision is the endpoint (what vertex is the last one).

Find the min cost path for involving a subset of vertices S and ending at e.

```python
# 1 not included because 1 is start point
minCostTSP(n) = min(
    ...minCostPath({2..n}, e)
)

def minCostPath(S, e):
    # in S choose some last point
    # solve TSP in the scope of S

# so the recurrence is
# minCostPath(S, e) = min(
#     (cost_of_s_to_e_directly +
#     minCostPath(S|s, s)) for all s in S (S|s means S without s so each recurrence shrinks the set by 1)
# )
```

The base case is when your set S has 0 or 1 elements. Then the min cost path is
obvious.

To memoize, create a table indexed by `S,e` and store the value and which
element gave you the min value.

To recover the solution, inspect the table from bottom to top reconstructing
from the last vertex to the first.

One of the fastest algorithms in the general case, but others can beat the
algorithm in practice.
