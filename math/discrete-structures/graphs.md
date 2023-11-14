# Graphs

Graphs are a data structure that come from [binary relations](./sets.md).

Vertices (nodes) are connected by edges (links). Ex: the edge (u,v) connects node u
to v. u is the tail and v is the head.

Every node has an in-degree (the number of edges pointing into it) and an
out-degree (the number of edges pointing out of it).

## Notation

Normally you just draw it out in a math context.

### Adjacency Matrix

```
0 0 1 0
1 0 0 1
0 1 0 0
1 1 0 1

shows if (from x, to y) is true
```

### Operations

#### Walk

Start at one vertex and use a sequence of edges to reach another vertex. The
length of a walk is the number of edges in the walk, not the number of nodes.

#### Circuit

A walk where the last vertex is the vertex you started at. <a> is a circut of
length 0.

A circuit is a cycle if there are no other repeated nodes other than the initial
and final node.

## Graph power theorem

Let G be a directed graph. Let u and v be any two vertices in G. There is an
edge from u to v in G^k (g composed with itself k times) if and only if there is
a walk of length k from u to v in G.

## Transitive Closure

If you have a graph with n vertices there is no direct path without loops
between two vertices that is longer than n.

I Need to find a better description of transitive closure algorithm.

## Directed Acyclic Graph

Graph with directed edges and no loops.

You can sort them with topological sort to show the dependency relations between
nodes.
