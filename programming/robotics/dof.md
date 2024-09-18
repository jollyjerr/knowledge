# Coordinate System and Degrees of freedom

How do you describe the pose of a robot?

The only full description is a total coordinate system.

You can thing about it with your right hand:

- Thumb along x-axis
- Index along y-axis
- Middle along z-axis

Order counts.

## Axis-Angle or Quaternion Notation

Three vertices (x, y, z) each with 3 values.

We only need 4 values to express rotations (9 values):

- Each column is a basis vector
- They are orthogonal -> the third vector is given by the other two
- They are normal -> the third value is given by the other two

## Degrees of Freedom

- Cartesian space

An airplane can be in all possible positions and orientations - 6 DoF.

A human arm can move in 6 DoF in cartesian space.

- Actuator Space

An airplane can pitch, roll, and accelerate along positive X - 3 DoF.

A human arm has 7 DoF in actuator space.
