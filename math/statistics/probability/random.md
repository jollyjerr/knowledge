# Random Variables

A random variable is a function that maps events from the sample space S to the
real numbers.

They can be discrete or continuous:

- Discrete if its set of possible values is discrete (number of coin flips)
- Continuous if its set of possible values is an entire interval of numbers
  (time between two customers entering a store)

Usually denoted by X or Y, and specific instances of the variable are x or y.

The "expected value" of a rv is the average or mean of the random variable.

Notation:

`E(X)` or `u sub x`

The "variance" of a random variable X, denoted V(X) measures how far we expect
our random variable to be from the mean.

```
V(X) = E[(X - E(X))^2]

= E(x^2) = (E(X))^2 <- the "second moment" minus the mean squared
```

The standard deviation is the positive square root of the variance.

## Discrete

The expected value of a discrete random variable `E(X)` is given by

```
E(X) = sum(k) kP(X = k)
```

### Probability mass function

A probability mass function of a discrete rv, X, is given by

```
P(x) = P(X = x) = P(all x in S | S(s) = x)
```

Each x is P less than 1, and the sum of all x is 1.

### Cumulative Distribution Function

```
F(y) = P(X <= y) = sum(x<=y)P(X = x)

so

example: 0=.05,1=.10,2=.15

f(y) = {
    0 if y < 0,
    .05 if 0 <= y <= 1,
    .15 if 1 <= y < 2,
    ...
}
```

## Bernoulli

Bernoulli, or binary rvs are any random variable with only two possible
outcomes: 0 or 1.

The probability mass function:

```
P(X = 1) = p
P(X = 0) = 1 - p
```

Cdf:

```
F(x) = P(X <= x) = {
    0 if x < 0
    1 - p if 0 <= x < 1
    1 if 1 <= x
}
```

Notation: `X ~ Bern(p)` means X has the distribution of a bernoulli random
variable.

`E(X)` for a bern is `p`

`V(X)` for a bern is `p(1-p)`

## Geometric

This happens when you are finding the probability that some n things will fail
before one succeeds.

Recall [geometric series](./../../calculus/series.md).

```
P(X=1) = p
P(X=2) = (1-p)p
P(X=3) = (1-p)^2 p
P(X=k) = (1-p)^(k-1) p <- probability mass function
```

Consists of independent Bernoulli trials, each with the same probability of
success p, repeated until the first success is obtained. The trials must be
identical and independent.

Sample space `1,01,001,0001,...`

Notation: `X ~ Geom(p)`

`E(X)` for a geom is:

```
sum(1, inf) kp(1-p)^(1-p)

and via some calc magic

= 1/p
```

`V(X)` for a geom is `1-p/p^2` via some mega super calc magic

standard dev is 9.5

## Binomial

- n bernoulli trials (n is fixed in advance)
- trials are identical and result in a success or a failure with P(success) = p
  and P(failure) = 1 - p
- Trials are independent (outcome of one trial does not influence any other)

```
X ~ Bin(n, p)

S = {(x1, x2, ..., xn) | xi = {1 if success on ith trial, 0 if failure}} 

# |S| = 2^n but each event is not equally likely

P(X = 0) = P({0..0}) = (1-p)^n
P(X = 1) = P({10...0, 010..0}) = np(1-p)^(n-1)
P(X = k) = P({k 1's and n-k 0's}) = (n choose k)P^k(1-p)^(n-k)

E(X) = np

V(X) = np(1-p)
```

In a _negative binomial_ variable you fix `r` (the number of successes) and
count the number of failed trials before success.

`X ~ NB(r, p)`

```
if Y ~ NB(r, p)

P(Y = k) = ((k+r-1) choose (r-1))p^r(1-p)^k for k = 0,1,2...

E(Y) = (r(1-p)/p)

V(Y) = (r(1-p)/p^2)
```
