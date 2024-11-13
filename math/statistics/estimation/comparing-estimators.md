# Comparing Estimators

Estimators normally are a trade off between variance and biased predictions.

## Mean Squared Error

Let `theta_hat` be an estimator of a parameter theta. The mean squared error of
`theta_hat` is denoted and defined by:

```
MSE(theta_hat) = E[(theta_hat - theta)^2]
```

If `theta_hat` is an unbiased estimator of theta its mean squared error is the
variance of theta.

The bias of `theta_hat` is denoted and defined by:

```
B(theta_hat) = E[theta_hat] - theta
```

## Relative efficiency

Let `theta_hat_1` and `theta_hat_2` be two unbiased estimators of a parameter theta.

`theta_hat_1` is more efficient that `theta_hat_2` if:

```
Var[theta_hat_1] < Var[theta_hat_2]
```

The relative efficiency of `theta_hat_1` to `theta_hat_2` is denoted as:

```
Eff(theta_hat_1, theta_hat_2) = Var[theta_hat_2] / Var[theta_hat_1]
```
