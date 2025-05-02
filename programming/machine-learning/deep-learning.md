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
