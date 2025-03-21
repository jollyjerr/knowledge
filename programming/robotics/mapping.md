# Mapping

Mapping is used for navigation and localization.

GPS and compass sensors make localization much easier.

Simultaneous Localization and Mapping (SLAM).

## Grid Mapping

Constant memory requirement of world. Fill in pixels if data says that pixel is
occupied.

```
Laser data (ranges and angles)
|
Transformation Point cloud
|
Discretization
|
NxN map
```

In discretization you derive a function to map extrema/bounds of sensor data to your
grid.

Can easily transform to a `K-d Tree (Quadtree)` to lower memory requirement.
Store and read are O(1) in quadtree because the depth is a constant.

Use a topological map for navigation data.

All grids can be turned into graphs, but not all graphs have grids.
