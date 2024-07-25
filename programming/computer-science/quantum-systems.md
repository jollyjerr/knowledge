# Quantum Systems

Need to read book by Radhika Vatnan.

## Single Qubit

A qubit is a unit of information; a quantum bit.

We describe states of matter as wave functions.

### Ket Vectors

A vector of all observable states is called a Ket vector, written as `|0>` where
you map 0 to a vector (in the Hilburt space) that describes a particular state
of an electron. Same for 1 `|1>`.

### Superposition

`|0> and |1>` are "pure" states. A quantum system can be in a superposition of
two states:

`a * |0> + b * |1>` where a and b are complex numbers called "amplitudes".

### Measurement

When you make a measurement:

- with probability `|a|^2` it collapses to `|0>`
- with probability `|b|^2` it collapses to `|1>`

Keep in mind that total probability will stay 1.

Once you measure the system, the superposition is gone forever (if you continue
to make the same measurement. In some cases a different axis of measurement
could change the measurement to uncertain again.)

### Operations

Quantum operations (or Unitary operations).

Hit `a` and `b` with a unitary matrix, resulting with a new superposition.

```
a` * |0> + b` * |1> = U(a|0> + b|1>)
```

A Unitary matrix is a 2x2 matrix of complex numbers. The matrix has to be it's
own inverse (it is a little more involved then that but a lot to write down here).

`U^+ * U = I`

## Multi Qubit
