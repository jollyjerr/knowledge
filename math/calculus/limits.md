# Limits

The limit of a function at any value x is the result that function approaches at the value x.

You can approach a limit from the left or right side, and if a limit exists it is called the general limit.

A limit is precisely defined as:

```
lim f(x) = L
x->a

if, for every number epsilon > 0 there is some number delta > 0 such that

|f(x) - L| < epsilon whenever 0 < |x-a| < delta
```

So a function at any value x does not have a general limit if the left and right hand limits do not approach a single value.

## Point discontinuities

```
Example:

f(x) = (x^2 - 4)/(x-2) // call this A

f(2) is undefined because division by 0 is undefined

yet...

(x^2 - 4)/(x-2) => ((x + 2)(x - 2))/(x - 2) => f(x) = x + 2 // call this B

So f(2) = 4

A and B have different behavior at x = 2.

B has the value of 4 at x = 2 while A approaches more and more closely to 4 at x = 2 from both the left and right hand side.
```

In this example A had a point discontinuity at x = 2 and we showed algebraically that this discontinuity is removable and therefore not a vertical asymptote.

This could also be a [piecewise defined function](../algebra/piecewise-defined-functions.md):

```
f(x) = {
    (x^2 - 4)/(x-2)       x != 2
    4                     x = 2
}
```

While general limits exist in point discontinuities, they do not exist for jump discontinuities or infinite discontinuities (asymptotes).
Although, sometimes asymptotes that both approach -Inf or +Inf will be described as having a limit of - or + Inf.

##### Aside, Intermediate Value Theorem

For any continuous function, given a closed interval, we can assume there is atleast one "root" (cross of x axis) if we can find a negative point and positive
point in that interval.

## Properties of limits

You can find the limit of any function or combination of functions:

```
lim f(g(x))
x->3
```

because limits respect these properties:

```
Because typing the limit symbol is hard, & = lim
                                             x->a

for any real number c, &[cf(x)] = c * &f(x)

&[f(x)±g(x)] = &f(x)±&g(x)

&[f(x)g(x)] = &f(x)&g(x)

if g(x) != 0 then &[f(x)/g(x)] = &f(x)/&g(x)

fon any real number n, &[f(x)]^n = [limf(x)]^n
```

Even if fx and gx both have undefined limits, you may be able to find a limit from their combination.
You can check this by finding their limit "from the left" and "from the right" and doing the calculation.
If both of them result in the same value, then that is the limit

```
if:

lim                 lim
x->a^- (fx + gx) == x->a^+ (fx + gx)

then that value is the limit

```

### Composite Limits

```
lim
x->1 f(g(x))
```

If the limit (L) defined by g(x) exists AND f is continuous at L, then your solution is

```
f(lim x->1 g(x))
```

If not, you can solve g(x) "from the left" and "from the right" to get two different inputs
(include the direction of approach in these inputs because it may swap! The y axis of this first result is the direction of approach for the input to f),
and then plug those inputs into f(your_input) and see if they converge on a single limit.

## Solving Limits

There are different methods you can use to solve limits.

### Substitution

If a function is always defined you may be able to just substitute the limit as the value.

```
lim log(x) == log(5)
x->5
```

### Factoring

When substitution does not work, you may be able to use factoring to show the continuous function.

```
lim (x^2-16)/(x-4)
x->4

// factor using difference of squares

(x-4)(x+4)/x-4

x+4

// now substitute

4+4 = 8
```

### Conjugate Method

If presented with a fraction that does not factor, the [conjugate](../algebra/radicals.md) method may be a good approach.

Conjugate = irrational side of fraction, flip the expressions _between_ each term.

Hot tip: don't distribute everything out right away, go slow and look for the point where you can cancel terms

After doing more of these problems I would say your goal is to work out the radical side of the fraction so that it can cancel out with the non radical side.
Use whatever tricks you can to cancel out the non radical side

```
lim (sqt(4+h)-2)/(h)
h->0

sqt(4+h)-2/h * sqt(4+h)+2/sqt(4+h)+2

...
```

[This](https://www.khanacademy.org/math/differential-calculus/dc-limits/dc-limits-algebraic/v/limits-by-rationalizing) khan video explains this method extremely well.

_Hot Tip_ If you find a limit `0/0` that is indeterminate form and does not mean the limit does not exist. Use a different method to find the limit if you have reached that answer.

## Pythagorean Identity

If you are solving a limit that uses pythagorean functions and you reach indeterminate form (0/0), you can substitute
[trig identities](../trigonometry/trig-identities.md) to try and cancel out terms and work the problem.

#### L Hopitals rule

When you cancel out terms with conjugate method or pythagorean identity you must remember to specify which value the new function does not work at

```
1-cosx/2sinx^2 -> 1-cosx/2(1-cos^2x) (a^2 - b^2 here difference of two squares) -> 1-cosx/2(1+cosx)(1-cosx) -> 1/2 + 2cosx where x != 0
```

And then you find an identical function that includes 0 in it's domain, and you know from the properties of limits that the identical function and your function will have
the same limit at x = 0. (if f(x) and g(x) are the same for all values except a and g(x) is continuous at a, then the limit of a is equivalent for both functions).

So just keep in mind the function you find from simplifying is not the function you use to solve at x because they have different domains but just happen to have identical limits.

## Strategies of finding limits

This is just a way of thinking about which of the various strategies discussed here you should use for any limit.

```
lim  f(x)
x->a
```

If f(a) = b/0 you probably have a vertical asymptote (check the graph to be sure)
If f(a) = b you probably have a limit b! (again, check the graph to be sure)
If f(a) = 0/0:
Try factoring to cancel terms
Try conjugates to cancel terms
Try trig identities to cancel terms

    Once you have canceled terms, evaluate the limit in it's new form (start this whole process over again as many times as necessary)

If all else fails, try approaching the limit from below and above

## Infinite Limits

There is a difference between infinite limits and "limits at infinity"

A limit at infinity refers to the limit of a function as the input approaches infinity.

An infinite limit refers to the function itself approaching infinity at a particular point.

Infinite limits exist around vertical asymptotes of a function.
