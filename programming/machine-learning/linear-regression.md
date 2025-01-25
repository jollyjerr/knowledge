# Linear Regression

A simple supervised learning model that makes predictions on linear
relationships.

- Predictive task: real valued numbers
- Parametric
- No hyper parameters
- Features have linear relationship to target variable

You predict a quantitative response Y on the basis of a single predictor
variable X:

```
Y is approximately modeled as B[0] + B[1]X
```

The B values (coefficients or parameters) are two unknown constants that represent the intercept
and slope.

By estimating the B values you can find an intercept and slope such that the
resulting line is close to your real data. The most common way of doing this is
minimizing the least squares criterion using mean squared error (MSE).

Other measures:

- mean absolute error
- mean percent absolute error
- root mean squared error

Let

```
y_hat[i] = B-hat[0] + B_hat[1]x[i]
```

Be the prediction for Y based on the ith value of X. Then `e[i] = y[i] - y_hat[i]`
represents the ith residual, the difference between the ith observed response
value and the ith response value that is predicted.

```
B[1] = Cov(X, Y)/Var(X)

B[0] = E[Y] - Cov(X, Y)/Var(x) E[X]
```

This resulting line is the least squares line which is different from the true
population line that would be produced if you could observe all data. The bias
is the drift between the least squares line and population line like in stats.

Multivariate case

```
MSE = ||y-xB||2

X^t(xB - y)
```

## Model fitness

`R^2` can be a measure of how well your model fits:

```
R^2 = 1 - RSS/TSS
```

## Summary

1. How to determine coefficients

Least squares method to minimize the residual sum of squares. RSS, Mean squared
error.

2. How well does the model fit

R-squared derived with RSS and TSS

3. How significant are the coefficients

Standard error of the coefficients. T-score, p-value and hypothesis testing to
find if they are significant. Confidence intervals.

4. How well does the model predict on unseen data
