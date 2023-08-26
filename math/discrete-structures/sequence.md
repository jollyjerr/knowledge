# Sequence

A sequence is basically a general list type mathematical tool that can be
indexed. It's technically a function where the domain is a consecutive set of
integers.

```
g: {1,2,3,4} -> R

g(1) = 3.98, g(2) = 4.0 etc...
```

Sequences can have positive or negative indexes.

They can be infinite or finite

## Formula

Sequences can be defined as a formula:

```
d(k) = 2^k where k = 0,1,2,3...
```

## Geometric sequence

A sequence of real numbers where each element is obtained by multiplying the
previous element by some common ratio.

```
a, ar, ar^2, ar^3, ar^4,...,ar^n
```

Compound interest is a geometric sequence

```
base_amount(1+rate)^years
```

## Arithmetic sequence

A sequence of real numbers where each element is obtained by adding a constant
to the previous element.

```
a, a+d, a+2d,..., a+nd
```

## Summation notation

```
t (upper limit)
∑ a[i]                       = a[s] + a[s + 1] + a[s + 2] + ... + a[t]
i = s (lower limit)
```

## Recurrence relation

When you cannot create a general formula for a sequence and need to refer to the
previous terms of the sequence

example: fibonacci sequence

```
f[0] = 0
f[1] = 1
f[n] = f[n-1] + f[n-2] for n >= 2
```
