# Mapping

Mapping is a function to take data space to a visual space.

## Data space

Datasets are formed of dimensions, and each dimension has a type.

The type informs effective mapping choices.

- Categorical: cats, dogs, birds
- Ordinal: small, medium, large
- Continuous: 1, 2, 3

## Visual space

AKA "Marks"

There are many:

- position
- color
- shape
- orientation
- size
- value/lightness
- motion
- texture

## Mapping strategy

- What visual encoding do we use?

- How do we compute the visual representation from the data value?

Expressiveness: Express all the data, but nothing else

Effectiveness: The importance of the attribute should match the salience of the
channel

### Tips

Log scales can help with uneven distributions of data, but can make your chart
harder to read.

Mapping data to size can be misleading. EX: twice as big diameter makes a circle
4 times as large in terms of area.

QTons: use shape complexity to represent a gradient of change. Texture density
helps show complexity increase.

Use motion very sparingly: direction, velocity, acceleration.

Texture: Density, variation, pattern

Color: Hue, chroma, luminance
