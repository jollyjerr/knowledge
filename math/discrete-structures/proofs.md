# Proofs

A theorem is a statement that can be proven to be true, and a proof is the
formal process of showing that it is true via a series of steps consisting of
axioms (assumed truth), proven theorems, and logic.

Writing proofs is formally done like:

```
Theorem:
Every positive integer is less than
or equal to its square.

Proof:
Let x be an integer, where  x > 0

Since x > 0, we can multiply both
sides of the inequality by x to get: x*x >= 1x

Simplify the expression we get: x^2 >= x ∎
```

## Language

Proofs use language to give the purpose of each line:

let/suppose: new variable
thus/therefore: it follows from the last point
since: restate a fact or assumption
we will prove/show: purpose
by definition
by assumption
in other words
gives/yields

## Universal Proofs

### Proof by Exhaustion

If you literally walk through every element of a domain and prove a statement is
true for each element, you have proven the universally qualified statement as
true via exhaustion.

### Universal Generalization

Name an arbitrary object of a theorem's domain and prove the theorem for that
object.

The example at the top of this document is a universal generalization.

Remember that you only need a single counterexample to prove universally
quantified statements as false. A counterexample needs to satisfy all the
hypotheses but contradict the conclusion.

## Existential Proofs

To disprove an existential statement you have to prove that for every element
the statement is false.

### Constructive proof of existence

Give a specific example of an element that has the required properties.

### Nonconstructive proof of existence

Commonly done by showing that assuming no element exists leads to a
contradiction.

## Direct Proofs

p -> c

p is assumed to be true and the conclusion is proven to be true as a direct
result of the proposition.
