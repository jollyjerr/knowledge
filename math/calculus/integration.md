# Integration

## Intuition

The [derivative](./derivatives.md) is taking a distance
function (position) and calculating it's velocity over time. Integration is the process of taking a
velocity function and deducing the distance traveled. Hence the nickname
"anti-derivative"

1. Given a position of an object, the derivative represents its velocity.
2. Given the velocity of an object, the area under the curve to the x axis
   represents it's position.

## Distance vs displacement

1. Distance is given by the area above the x-axis **plus** the area below the
   x-axis.
2. Displacement is given by the area above the x-axis **minus** the area below the
   x-axis

Displacement is also sometimes called the "signed area between a graph and the
horizontal axis".

Integration is typically interested in displacement.

When the velocity function dips below the x axis, the area under that negative
portion of the curve should typically be subtracted from your final answer
because it is negative velocity.

Intuitively if you run 3 miles and turn around and run 2 miles your displacement
is only 1 mile.

## Approximation

Let's say we have a velocity function `f(x) = x(8-x)`

### Endpoint Approximation

Remember `distance = velocity * time` and the area of a rectangle is `area = x * y`

We can approximate the distance traveled over an interval by breaking the
interval into rectangle and calculating the distance of each rectangle.

For each rectangle you can pick an approximation of the velocity at any point in the
rectangles width `f(x) where x is inside rectangle`:

left side = left-endpoint approximation
right side = right-endpoint approximation
any point in the middle would also work.

If you calculate the distance (area) of **each** rectangle at left-endpoint and at right
endpoint, you know that the real answer is somewhere between those two
answers.

### Improving the Approximation

If you take endpoint approximation and imagine approaching infinite rectangles
or the width of each rectangle approaching 0 you can calculate the actual area
under the curve.

#### Infinite Rectangles

Define a rectangle as `width: deltax, height: f(n)`

Suppose f(x) is a continuous function on [a,b]. Divide the interval into n
subintervals. The width of each subinterval is `deltax = (b-a)/n` (b-a is length
of full interval and you divide by number of rectangles)

#### Width of each rectangle approaching 0
