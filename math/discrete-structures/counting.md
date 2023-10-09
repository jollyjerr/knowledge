# Counting

In discrete mathematics the goal of counting is to count the number of elements 
in (or the cardinality of) a finite set given a description of the set.

## Product rule

To count sequences you use the product rule. How many unique combinations of
elements? Multiply them:

```
A, B, C be finite sets, then
|A| * |B| * |C|
```

This can be used when limiting string characters and other similar stuff, so if
there are 26^3 3 letter words, there are 26^2 * 2 three letter words that begin
with a or b.

The _generalized counting rule_ considers the impact of selecting an item on the
cardinality of the next choice. So if you have 20 runners in a race and want to
see how many podium outcomes exist, it is not 20 * 20 * 20 but 20 * 19 * 18.

## Sum rule

When only one element is selected, not combinations of elements, you just add
the cardinality of each set to get the number of outcomes.

|A ∪ C| + |B|

Sum and product rule example:

```
Each character in a password is either a digit or lowercase letter. How many
valid passwords are there if the length can either be 10 or 8 and every password
must start with a digit?

(36^9 * 10) + (36^7 * 10)
10(36^9 + 36^7)
```

## Bijection rule


