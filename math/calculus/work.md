# Work

One of the main applications of [integration](./integration.md) in engineering and physics is
computing work.

work = force * distance if the force is constant. Special case of:

work = ∫force

In real life you always have a variable force.

## Houke's Law (spring extension problems)

```
f= kx

force = (spring constant) * (distance past resting)
```

If you have a 3m spring and you stretch it to 7m, how much work did it take?

k = 1.5

```
integrate from not streatched to distance past resting of 4 (7m-3m)

w = ∫[0,4] 1.5x dx

1.5(x^2/2)

12 jules
```

If the problem does not give you k, you likely have to figure it out from other
information:

"It takes 20N of force to extend 15m"

```
recall f = k * x

so 20 = k * 10

so k = 2
```

## Bucket on a rope problems

A bucket weighs 4N and is hanging at the bottom of a 6m length of rope. The rope
weighs (density) 1.5N/m. How much work does it take to pull up the bucket?

Force is changing because the amount of rope you have to pull is always
changing.

```
w = ∫f

w = ∫[0,6] 4 + 1.5(6-y) dy

break up into bucket and rope

∫[0,6]4dy + 1.5∫[0,6]6-y dy

(4*6) + 1.5(6y-(y^2/2))|[0,6]
```

What about if it is raining and filling up the (initially empty) bucket at 2N/s and the bucket is
being raised at 1m/s and the bucket can hold 8N of water?

```
w = ∫Fbucket + ∫Frope + ∫Fwater before full + ∫Fwater when full

for the integral of force of water, think about how every meter the bucket goes
up there is 2N of water filling the bucket because the rates have the same unit

∫[0,6] 4 dy + ∫[0,6] 1.5(6-y) dy + ∫[0,4] 0 + 2y dy + ∫[4,6] 8 dy

for the upper bound on the water before full limit:

bucket stops filling when 2y = 8

y = 8/2 = 4
```
