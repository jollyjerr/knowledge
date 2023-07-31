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

```
∫kdx = kx + C
∫dx = x + C
```

### Power functions

```
∫x^ndx = [x^(n+1)/(n+1)] + C when n != -1
```

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

```
∫(f(x) + g(x))dx = ∫f(x)dx + ∫g(x)dx
∫(f(x) - g(x))dx = ∫f(x)dx - ∫g(x)dx
∫cf(x)dx = c∫f(x)dx
```

### Exponential and logarithmic

```
∫e^x dx = ex + C
∫a^x dx = (a^x)/ln(a) + C
∫1/x dx = ln(|x|) + C
```

### Trigonometric

```
∫sinx dx = -cosx + C
∫cosx dx = sinx + C
∫sec^2(x) dx = tanx + C
∫secxtanx dx = secx + C
∫-cotxcscx dx = cscx + C
∫-csc^2x dx = cotx + C
∫1/(sqrt(1-x^2)) dx = sin^-1(x) + C = arcsinx + C
∫1/(1+x^2) dx = tan^-1(x) + C = arctanx + C
```

## Initial Value Problems

Sometimes you are provided with an initial value(s) so that the family of
antiderivatives can be narrowed down to a single antiderivative.

Find f(x) if f'(x) = cos(x) + sin(x) and f(0) = 5.

Initial values are also helpful because you can graph the resulting function.

## Average value of a function

aka average slope of all tangent lines of the derivative

signed area/width -> (∫[interval]f(x)dx)/interval

```
avg value of f(x) on interval [a, b]
take (∫[a to b]f(x)dx)/b - a
(F(b) - F(a))/b - a
```

## U Substitution

Some functions can not be integrated using the above rules but you can use a
process called u-substitution.

This can only work if the function has one "chunk" that **is the derivative** of
another "chunk" of the function. For example: in `∫3x^2(x^3 + 5)^7 dx` `3x^2` is
the derivative of `x^3 + 5`. The chunk will almost always be the longest x
expression that is composed inside another function, like `x^7` in this case.

1. Define a new variable `u` to be the chunk of the function that has it's
   derivative in the function, so in this case `u = x^3 + 5`
2. Take the derivative of u. `du = 3x^2 dx`
3. If `du` does not exist exactly in the remaining function, you have to
   manipulate `du` and/or `u` algebraically until you have exactly what you need
   for the substitution to work out. See other examples for this.
4. Now that you have u and du, substitute into the original function: `∫(u^7)du`
5. Integrate this new function: `((u^8)/8) + C` The `du` is removed here because
   you inverted the chain rule behind the scenes.
6. Back substitute `u` and simplify if you can: `(((x^3 + 5)^8)/8) + C`

**Check the definite integral example to see special steps for definite
integrals**

### Examples

#### Rearrange the du expression

```
∫(x^3)/sqrt(1 - x^4) dx

u = 1 - x^4
du = -4x^3 dx

-4x^3 does not exist in the original expression

(-1/4)du = x^3 dx

now it does :), so substitute

∫((-1/4)du)/sqrt(u)

-1/4∫(1/u^1/2)du

-1/4∫(u^(-1/2))du

now integrate

-1/4(u^1/2 / 1/2) + C

simplify

-1/4(2)u^1/2 + C

back substitute u

-1/2(1 - x^4)^1/2 + C
```

#### Rearrange the u expression

```
∫xsqrt(x + 2) dx

u = x + 2
du = dx

rearrange u so you can substitute

x = u - 2

now substitute

∫(u - 2)sqrt(u) du

simplify

∫(u - 2)u^1/2

∫u^3/2 - 2u^1/2 du

integrate

(u^5/2 / 5/2) - (2c^3/2 / 3/2) + C

simplify

(2/5)u^5/2 - (4/3)u^3/2 + C

back substitute

(2/5)(x + 2)^5/2 - (4/3)(x + 2)^3/2 + C
```

#### Trig

```
∫sinx/cos^3x dx

u = cosx
du = -sinx dx -> -du = sinx dx

∫-du/u^3 = -∫1/u^3 du = -∫u^-3 du

integrate

-(u^-2 / -2) + C = (1/2)u^-2 + C = (1/2u^2) + C

back substitute

(1/(2cos^2x)) + C
```

#### Definite integral

As soon as you get rid of the x variables and replace them with u variables, you
need to adjust the limits by plugging them in for `x` in the `u` expression.

```
∫[0 to 2]2x(x^2 + 4)^2 dx

u = x^2 + 4
du = 2xdx -> du/2x = dx

∫[0 to 2]u^2 du // dx canceled out

adjust limits

u = 0^2 + 4 = 4 -> lower limit is 4
u = 2^2 + 4 = 8 -> upper limit is 8

∫[4 to 8]u^2 du

evaluate

(8^3 / 3) - (4^3 / 3)

448/3
```

## Integration by parts

This expression is true:

```
∫u dv = uv - ∫v du

or written as

∫f(x)g'(x) = f(x)g(x) - ∫g(x)f'(x)
```

And you can use it to rewrite integrals so they are solvable

```
∫xe^x dx

u  = x
dv = e^x dx
du = 1 dx <- derivative of u
v  = e^x <- intigrate dv (+C does not matter here)

∫xe^x dx = xe^x - ∫e^x dx

now solve the new equation

xe^x - e^x + C
```

If you are struggling to pick u and dv, follow LIATE in order and take something
of that type for u. u should get simpler when you take the derivative and dv
should not get more complicated. dv always gets the dx.

- L logs
- I inverse trig
- A algebraic
- T trig
- E exponential

Sometimes you have to do integration by parts multiple times until you get
something you can integrate.
