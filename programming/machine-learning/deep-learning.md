# Deep Learning

This is "the book" https://www.deeplearningbook.org/

## Perceptron

Deep learning neural networks are loosely based on neurons in biological brains,
but are developed my mathematics and statistics.

A perceptron is on "neuron" with input from others, with weights, and an activation function
to control the output.

### Perceptron rule

```
f(sum_j W_j - X_j + b)
```

Weights are the normal vector for the decision boundary.

1. Cycle through training data
2. Update W on misclassified instances
3. (positive misclassified as negative) `W = W + X_i`
4. (negative misclassified as positive) `W = W - X_i`

### Delta rule (gradient descent)

```
W_j <- W_j + deltaW_j
```

### Linearly inseparable cases

Like `XOR` gate.

Can be solved by combining neurons - making layers.

Decision boundaries draw shapes in the vector space.

Typically the activation function is the same for a full layer of a neural
network.

Called MLP - can approximate any nonlinear function.

### Back propagation

Use chain rule to update inner layers from error.

Real implementations use the "computation graph" with "autodiff".

## Optimization Methods

Find a set of optimized weights which minimize the error (or loss function) at
the output.

Hyper parameter tune the learning rate.

### Stochastic Gradient Descent (SGD)

Use mini batches of data to each weight to update it's calculation. Mini batches
should be reasonable size to achieve best training efficiency.

Estimate gradient with SGD gradient formula from batch and corresponding
targets.

Introduces problem: "learning rate scheduling".

Adding the momentum "moving average" can make it faster. Makes learning converge
on optimum faster.

Read `keras` documentation on SGD for more information on specific
implementation.

Nestrov momentum does early correction on gradient.

Also check out learning rate normalization techniques like Adadelta.
