# Taylor Series

The Taylor series of a function f(x) is a certain [power series](./series.md) that equals f(x).

```
f(x) = sum(0, inf) (f^(n)(0))/n! x^n

where f^(n)(0) is the n-th derivative of f(x) evaluated at 0
```

For the n-th derivative bit: take higher order derivatives of f(x) until you see a pattern
(normally 4?) and then evaluate all of them at 0. If they all equal the same
thing then just use that, but if not you should be able to express them in terms
of x.

```
skipping some steps but this is the vibe

f(x) = 1/x

f'''(x) = (2 * 3) / (1 - x)^4

sum(0, inf) n!/n! x^n

sum(0, inf) x^n where |x| < 1
```

## Common Taylor Series

```
e^x = sum(0, inf) x^n/n! // for all x

1/(1-x) = sum(0, inf) x^n  // where |x| < 1

sin(x) = sum(0, inf) (-1)^n/(2n+1) x^(2n+1) // for all x

cos(x) = sum(0, inf) (-1)^n/2n! x^(2n) // for all x
```
