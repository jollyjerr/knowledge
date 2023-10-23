# Series

A series is just a sum.

## Sigma notation

```
5        <--- stop
󰒠 1/n^2  <--- formula for terms
n=1      <--- start
```

## Geometric Series

In a geometric series, the formula for terms is a number raised to the power
of the variable:

```
(1/2)^n
4(-6/8)^n

abstract:
󰒠 ar^n
```

Geometric series have a cool trick for solving them quickly:

1. Write out the original (partial is fine)
2. Write the same thing but with both sides multiplied by r
3. Subtract line 2 from line 1
4. Solve for the sum

```
sum((1/2)^n, 0, 3000) = (1/2)^0 + (1/2)^1 + ... + (1/2)^3000
- 1/2 sum((1/2)^n, 0, 3000) = (1/2)^1 + (1/2)^2 + ... + (1/2)^3001

things cancel...

1/2 sum((1/2)^n, 0, 3000) = (1/2)^0 - (1/2)^3001

sum((1/2)^n, 0, 3000) = [1 - (1/2)^3001]/(1/2)
```

## Infinite Series

An infinite series is just a limit where the stop value of the sum is your limit.

This example uses a general version of the geometric series example above:

```
sum((1/2)^n, 0, infinity)

lim[m->inf] [1 - (1/2)^(m+1)]/(1/2)

[1 - 0]/(1/2)

2
```
