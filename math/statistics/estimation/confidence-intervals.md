# Confidence Intervals

When giving a confidence interval, the randomness is in the sampling. Multiple
samples will result in multiple different confidence intervals. The percentage
of confidence is how many intervals from samples will actually contain the real
mean.

## Normal

```
Suppose Xn is a random sample from the normal distribution with mean u and
variance o^2.

Assume that o^2 is known.

- X_bar is an estimator of u
- X_bar is N(u, o^2/n)

X_bar-u / o/sqrt(n) ~ N(0, 1)

Suppose that Z ~ N(0, 1)

P(-1.96 < Z < 1.96) = 0.95

Solve for u in the middle

A 95% confidence interval for the mean u of a normal distribution is given by:

(
    X_bar - 1.96(o/sqrt(n)), # pnorm
    X_bar + (o/sqrt(n))      # qnorm
)

This can be written as:

X_bar +- 1.96(o/sqrt(n))

1.96 is called a critical value. z[a] be the # that cuts off area a to the
right.

-Z[a/2] < 1-a < Z[a/2] # -1.96 and 1.96 respectively in above example

So finally:

Suppose that X[1], ..., X[n] is a random sample from the normal distribution
with mean u and variance o^2.

A 100(1-a)% confidence interval for u is given by:

X_bar +- Z[a/2] * o/sqrt(n)
```

The example above assumes you have a normal distribution, so use the CLT to get
there.

```
Suppose that X[1], ..., X[n] is a random sample from any distribution with mean
u and variance o^2 < inf.

For large n, an approximate 100(1-a)% confidence interval for u is given by:

X_bar +- Z[a/2] * o/sqrt(n)
```

## Chi Squared

```
Let X ~ N(0, 1)
Let Y = X^2
Then Y ~ chi^2(1)
```
