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
there are 26^3 3 letter words, there are `26^2 * 2` three letter words that begin
with a or b.

The _generalized counting rule_ considers the impact of selecting an item on the
cardinality of the next choice. So if you have 20 runners in a race and want to
see how many podium outcomes exist, it is not 20 _ 20 _ 20 but 20 _ 19 _ 18.

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

If there is a [bijection](./functions.md) from one set to another then the sets
have the same cardinality. So if you can show there is a bijection then counting
an easy set can find the count to a difficult set.

This get's expanded to the "k-to-1" rule where one set will be the same
cardinality of another set multiplied by a constant factor k. Ex: each person
has two shoes. Then |B| = |A|/k.

## Counting Permutations

A permutation is a sequence that contains each element of a finite set exactly
once.

The number of permutations of a set with n elements is n!.

An r-permutation is a sequence of r items with no reputations all taken from the
same set.

There are n!/(n-r)! r-permutations to a set with n elements. A simplified form
of this counting procedure is show in code below.

```js
function p(options, length, depth = 0, result = 1) {
	if (depth === length) return result;
	return p(options - 1, length, depth + 1, result * options);
}
```

```
A red, blue, and green die are thrown. Each die has six possible outcomes. How many outcomes are possible in which the three dice all show different numbers?
6 * 5 * 4 = 120
```

## Counting subsets

If order does not matter, only the number of selected items, then you do not
count permutations and rather count subsets or "r-combinations".

Basically, tuples are permutations and sets are subsets.

You count them using the k-to-1 rule:

`r-permutations/r!` where r is the subset size

```
{1,2,3}

r-permutations: 6 (3*2*1)
r-combinations: 3 (6/2!)
```

Sometimes you see "n-choose-r" notation to mean the same thing:

```
(n r) = n!/(r!(n-r)!)
```

Where n is the number of elements and r is the subset size.

```js
function choose(n, r) {
	const factorial = (a) => {
		let result = 1;
		do {
			result *= a;
			a--;
		} while (a > 1);
		return result;
	};

	return factorial(n) / (factorial(r) * factorial(n - r));
}
```

Interesting bijection: n choose r == n choose (n-r) for non negative n
