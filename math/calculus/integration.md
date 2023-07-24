# Integration

## Geometry

Sometimes you can integrate a function easily by taking it's geometry.

For example, `int1-3(y=x-1)dx` is just a triangle so the answer is (2\*2) / 2

Also `int0-1(y=sqrt(1-x^2))dx` is the top half of a circle `x^2 + y^2 = 1`.
Given the range you are taking 1/4 of the area of the circle so `(pi(1)^2)/4 =
pi/4`.

## The Fundamental Theorem of Calculus

If f is continuous on the interval [a, b] and f(x) = F'(x), then
inta-b(f(x)dx) = F(b) - F(a)

The function F(x) is known as the antiderivative of f(x)

## Indefinite Integrals

When you find anti-derivatives you just use the existing [differentiation rules](./differentiation.md)
but in reverse.

example: f(x) = 2x has a family of antiderivatives F(x) = x^2 + C

### Constant

∫kdx = kx + C

∫dx = x + C

### Power functions

∫x^ndx = [x^(n+1)/(n+1)] + C when n != -1

Keep in mind all the rules of fractions and exponents so you can jump around

Example:

```
1/x^(9/4)
x^(-9/4)
(1/(-9/4 + 4/4))x^(-9/4 + 4/4)
(1/(-5/4))x^(-5/4)
(-4/5)x^(-5/4)

-4/(5x^(5/4))
```

### Sums, differences, constant multiples

∫(f(x) + g(x))dx = ∫f(x)dx + ∫g(x)dx
∫(f(x) - g(x))dx = ∫f(x)dx - ∫g(x)dx
∫cf(x)dx = c∫f(x)dx

### Exponential and logarithmic

∫e^x dx = ex + C
∫a^x dx = (a^x)/ln(a) + C
∫1/x dx = ln(|x|) + C

### Trigonometric

∫sinx dx = -cosx + C
∫cosx dx = sinx + C
∫sec^2(x) dx = tanx + C
∫secxtanx dx = secx + C
∫-cotxcscx dx = cscx + C
∫-csc^2x dx = cotx + C
∫1/(sqrt(1-x^2)) dx = sin^-1(x) + C = arcsinx + C
∫1/(1+x^2) dx = tan^-1(x) + C = arctanx + C
