# Optimization

local minimum: if f(p) <= f(near p) then point p is a local minimum of f
local maximum: if f(p) >= f(near p) then point p is a local maximum of f

## Critical Points

A point is a critical point of a function if the derivative of
the function at that point is zero or if it does not exist.

To find critical points of a function, take the derivative and set it equal to 0
and solve for x. Then try to find any points where the derivative is undefined.

```
f(x) = x - ln(x)
f'(x) = 1 - 1/x

1 - 1/x = 0 <-- a critical point exists at x = 1
1 - 1/x = undefined <-- a critical point exists at x = 0
```

## First Derivative Test

You can use the behavior of a functions first derivative to define local
maximums and minimums.

```
f'(x) < 0, local minimum, f'(x) > 0
f'(x) > 0, local maximum, f'(x) < 0
if the sign does not change, there is no relative max or min
```

To solve problems with this:

1. find your function's critical points and
2. plug in numbers to the left and to the right of critical points to see the behavior
   of the derivative around that point and determine if the critical point is a
   local min, local max, or neither.
3. if the point is a min or max, take it as the x value and plug back in to the
   original function to find the coordinates (x, f(x)).
