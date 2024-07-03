# RSA

## Euclid's Algorithm

```python
# GCD(m,n) = largest natural number that divides both m and n

# with m >= n
# GCD(m, n) = {
#     m               if n = 0
#     GCD(n, m mod n) otherwise
# }

def gcd(m, n):
    assert m >= n
    while n > 0:
        (m, n) = (n, m % n)
    return m
```

Runs in linear time to the number of bits in m.

## Bezout Coefficients

```
GCD(69, 15) = 3

so

3 = 15 * x + 69 * y

x = 9
y = 2

(9, 2) = GCD
```

so all `(15a + 69b)` must be divisible by the GCD

a and b are called Bezout Coefficients

You can find Bezout Coefficients with the extended Euclid's Algorithm

```python
def extended_gcd(a, b):
  if b == 0:
    return a, 1, 0

  gcd, x1, y1 = extended_gcd(b, a % b)

  x = y1
  y = x1 - (a // b) * y1

  return gcd, x, y
```
