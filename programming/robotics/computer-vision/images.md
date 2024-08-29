# Images

## Binary Image

Translate the screen into pixels, set them to 1 if they are totally filled.

## Gray scale Image

Use 255 bits to represent intensity between white and black for each pixel of
the screen.

## Binary Mask

Set pixel to 1 in foreground shape.

## Color Image

Three channels, RGB, each have map of screen pixels.

If a pixel should be black, `(0,0,0)` tensor.

Adjust each value in the range of 255 bits for each channel.

## Depth Map

Each pixel indicates how close or far from the camera, set up like gray scale.

## Image Functions

A function that maps a location to an intensity value.

```
# silly examples

f(x, y) = x + y

f(x, y) = {
    1 if |x| <= 1
    0 otherwise
}
```

### Operations

You can perform operations on the image function.

- flip: `f(x, y) => f(-x, y)`
- negate: `f(x, y) => 1 - f(x, y)`
- add: `f(x, y) => f(x, y) + 10`

You can combine operations, add two images, etc....

Also set operations like union is called masking.

`⨂` indicates a "cross correlation".
