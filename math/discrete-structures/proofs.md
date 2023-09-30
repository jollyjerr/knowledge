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

example:

```
Theorem: The difference between two even integers is even.

Let x and y be even integers. We will prove that x-y is even.

Since x is even, there is an integer k such that x = 2k.
Since y is even, there is an integer j such that y = 2j.

x-y = 2k - 2j

2k - 2j = 2(k-j)

Since k and j are integers, k-j is also an integer.

Since x-y is equal to 2m, where m = k-j which is an integer, x-y is even.
∎
```

## Contrapositive

To prove p -> q show that ¬q -> ¬p

Do this when ¬q is a more useful assumption than p.

If you have to negate and/or statements you can remember de morgan's laws:

```
If x < 0 and xy > 0, then y < 0.

contrapositive:

assume y >= 0, show x >= 0 or xy <= 0
```

## Contradiction

A proof by contradiction is an indirect proof where you assume the theorem is
false (¬t) and prove that a contradiction arises as a result of that assumption
(r ∧ ¬r).

## Proof by cases

For a universal statement, you can break the domain into different groups and
prove the theorem is true for a member of each group.

```
For every integer x, x2 - x is an even integer.

Case 1: x is even
Case 2: x is odd
```

Also you can sometimes break into one case without loss of generality:

```
Theorem: For any two integers x and y, if x is even or y is even, then xy is even.

Proof:
Without loss of generality, assume that x is even. Then x = 2k for some integer k. Plugging in the expression 2k for x in xy gives xy = 2ky = 2(ky). Since k and y are integers, ky is also an integer. Since xy is equal to two times an integer, xy is even.  ■
```
