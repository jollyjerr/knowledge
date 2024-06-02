# Integer Linear Programming

> LP + Integrality Constraint

The restriction is that the decision variables all have to be integers (they can
be positive or negative but must be whole numbers (set Z)).

## Example: Knapsack

List of items where each item has value and weight. You want to max value
without breaking the weight limit W.

Knapsack is NP Hard - the dynamic solution is pseudo polynomial time.

To approach this as an ILP problem:

```
# indicator decision variables
x sub i = {
    0 if Ii is not picked
    1 if Ii is picked
}

maximize v1x1 + v2x2 + v3x3 ... + vnxn

s.t. w1x1 ... <= W
     x1...xn member of Z
```

This is called a 0/1 or binary LP because the decision variables can only be 0
or 1.

## LP Relaxations

If you have an ILP and remove the integrality constraint, that is called lp
relaxation.

- `Opt. LP solution is always more optimal than Opt. ILP solution` every solution of an ILP
  is a solution of the LP
- If an LP relaxation is infeasible then the ILP is infeasible.
- If an ILP is unbounded than the LP relaxation is also unbounded.

## Integrality Gap

```
gap = opt(LP)/opt(ILP) for maximization problems
gap = opt(ILP)/opt(LP) for minimization problems
```

You cannot _always_ prove a bound on how large the gap is because some
optimization problems result in massive gaps (could even be infinite).

## NP Completeness

ILP solving is NP-hard

Decision problem: `is there a solution where the objective function is >= k ?`

- BinaryILP is a member of NP

The certificate is the value of each decision variable.

- BinaryILP is NP Complete

3-SAT can be reduced to BinaryILP.

Each clause of 3-SAT can be written as a constraint, and then you maximize the
number of clauses that are true by choosing "true" or "false" (0,1) for each "P"
value in each clause (so each P value is a decision variable and each clause is
a decision variable).

Therefore if you solved this ILP you would have a solution to 3SAT.

Most real world ILP algorithms run in exponential time.

## Vertex Cover Problem

Choose a subset of vertices that covers the graph (every edge touches one
selected vertex). Goal is smallest cardinality of subset.
