# Tests

## One-Tailed Tests

Let `X[1],...,X[n]` be a random sample from the normal distribution with mean u
and known variance `o^2`.

Consider testing the simple versus composite hypotheses.

```
H[0]: u = u[0]
H[1]: u < u[0]

(where u[0] is fixed and known)
```

1. Step One: Choose an estimator for u.

For example, the sample mean.

`u_hat = X_bar`

2. Step Two: Give the "form" of the test.

```
Reject H[0], in favor of H[1] if X_bar < c,
where c is to be determined.
```

3. Step Three: Find c.

Alpha is the maximum probability of making a type 1 error.

```
a = maxP(Type I Error) where u=u[0]
  = P(Reject H[0]: u[0])
  = P(X_bar < c: u[0])

X_bar is normal because it is a linear combination of normals.
We are assuming the true mean is u[0]
Therefore: X_bar ~ N(u[0], o^2/n)

  = P([(X_bar-u[0])/(o/sqrt(n))] < [(c-u[0])/(o/sqrt(n))]: u[0])
  = P(Z < [(c-u[0])/(o/sqrt(n))])

Critical value = Z[1-a]

c = u[0] + Z[1-a](o/sqrt(n))
```

If the null hypotheses is composite:

You have to reason your way to define the critical value, in general you will
need to use calculus for this. In straightforward problems, the result is the same as the
simple case.

4. Step Four: Conclusion

```
Reject H[0], in favor of H[1], if

X_bar < u[0] + Z[1-a](o/sqrt(n))
```

Finding the probability of this last statement is the "power function" and shows you the
probability that you reject the null hypotheses if it is false and the
probability that you fail to reject the null hypotheses if it is true.

### P Values

In 2019 the average health care annual premium for a family of 4 in the US was
reported to be $6,015. In a more recent survey, 100 randomly sampled families of
4 reported an average annual health care premium of $6,537. Can we say that the
true average is currently greater than $6,015 for all families of 4?

`o = 814`

Our size `0.10` test said to reject `H[0] if X_bar > 6119.19`. Our observed
sample mean was `x_bar = 6537`.

P value is an area in the tail based on where your critical value is.

```
P(Z > 634127)
```

Small P value means you reject the null hypotheses, and super tiny p values give
you a lot of confidence. Compare the p value to your value for alpha.

## Two Tailed Tests

Let `X[1],...,X[n]` be a random sample from the normal distribution with mean u
and known variance `o^2`.

Derive a hypothesis test of size a for testing:

```
H[0] : u = u[0]
H[1] : u != u[0]
```

We look at sample mean and reject if it is either too high or too low.

Form of test:

```
Reject H[0] in favor of H[1] if either X_bar < c or X_bar > d for some c and d
to be determined.

Easier to make it symmetric:

Reject H[0] in favor of H[1] if either X_bar > u[0] + c or X_bar < u[0] - c for
some c to be determined
```

Find c.

```
a = max(P(Type I Error))
  = P(Reject H[0]; u[0])
  = P(X_bar < u[0] - c or X_bar > u[0] + x; u[0])
  = 1 - P(u[0] - c <= X_bar <= u[0] + c; u[0])
1 - a = P(-c/(o/sqrt(n)) <= Z <= c/(o/sqrt(n)))

c = Z[a/2](o/(sqrt(n)))
```
