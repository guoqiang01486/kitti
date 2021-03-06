### Sampling of 000274.png:


##### Left
<img src="images/left/000274.png" width=900>

##### Right
<img src="images/right/000274.png" width=900>

##### Left - 3 temporally preceding frames (left color)
<img src="images/left_prev3/000274_01.png" width=900>
<img src="images/left_prev3/000274_02.png" width=900>
<img src="images/left_prev3/000274_03.png" width=900>

##### Right - 3 temporally preceding frames (right color)
<img src="images/right_prev3/000274_01.png" width=900>
<img src="images/right_prev3/000274_02.png" width=900>
<img src="images/right_prev3/000274_03.png" width=900>

##### <a name="labels"></a>Labels
Excerpt from the devkit_object readme describing the labels:
~~~~
#Values    Name      Description
----------------------------------------------------------------------------
   1    type         Describes the type of object: 'Car', 'Van', 'Truck',
                     'Pedestrian', 'Person_sitting', 'Cyclist', 'Tram',
                     'Misc' or 'DontCare'
   1    truncated    Float from 0 (non-truncated) to 1 (truncated), where
                     truncated refers to the object leaving image boundaries
   1    occluded     Integer (0,1,2,3) indicating occlusion state:
                     0 = fully visible, 1 = partly occluded
                     2 = largely occluded, 3 = unknown
   1    alpha        Observation angle of object, ranging [-pi..pi]
   4    bbox         2D bounding box of object in the image (0-based index):
                     contains left, top, right, bottom pixel coordinates
   3    dimensions   3D object dimensions: height, width, length (in meters)
   3    location     3D object location x,y,z in camera coordinates (in meters)
   1    rotation_y   Rotation ry around Y-axis in camera coordinates [-pi..pi]
   1    score        Only for results: Float, indicating confidence in
                     detection, needed for p/r curves, higher is better.
~~~~
Some samples:

| type       | truncated | occluded | alpha |    left |    top |   right | bottom | height | width | length |      x |     y |     z | rotation_y | score |
|------------|-----------|----------|-------|---------|--------|---------|--------|--------|-------|--------|--------|-------|-------|------------|-------|
| Car        |      0.00 |        0 | -1.59 |  586.42 | 199.76 |  662.87 | 266.02 |   1.36 |  1.69 |   3.38 |   0.28 |  2.08 | 17.74 |      -1.58 |       |
| Car        |      0.00 |        1 |  2.13 |   78.22 | 195.25 |  239.59 | 268.19 |   1.59 |  1.72 |   3.86 | -11.46 |  2.22 | 18.60 |       1.58 |       |
| Cyclist    |      0.00 |        3 |  2.48 | 1005.81 | 190.32 | 1206.35 | 331.10 |   1.68 |  0.86 |   2.01 |   6.30 |  1.92 |  9.28 |       3.06 |       |
| Van        |      0.00 |        3 | -1.72 |  700.62 | 162.16 |  807.39 | 261.63 |   2.12 |  1.86 |   4.41 |   3.34 |  1.93 | 17.73 |      -1.54 |       |
| Pedestrian |      0.00 |        0 |  0.15 |  389.42 | 179.08 |  424.76 | 303.37 |   1.87 |  0.64 |   0.65 |  -3.21 |  1.97 | 11.22 |      -0.13 |       |
| Van        |      0.00 |        3 |  1.99 |  258.72 | 187.25 |  349.36 | 238.52 |   1.71 |  1.56 |   4.12 | -11.33 |  2.28 | 26.92 |       1.59 |       |
| Car        |      0.00 |        1 | -2.17 |  370.32 | 190.97 |  497.81 | 255.70 |   1.59 |  1.63 |   3.64 |  -4.95 |  2.11 | 19.92 |      -2.41 |       |
| Car        |      0.00 |        2 | -2.33 |  394.24 | 197.69 |  512.54 | 247.36 |   1.41 |  1.64 |   3.61 |  -5.06 |  2.23 | 23.01 |      -2.55 |       |
| Car        |      0.00 |        2 | -2.30 |  425.76 | 196.25 |  535.81 | 239.43 |   1.39 |  1.61 |   4.09 |  -4.78 |  2.27 | 26.19 |      -2.48 |       |
| Car        |      0.00 |        2 | -2.27 |  477.24 | 194.55 |  553.19 | 229.87 |   1.50 |  1.57 |   3.54 |  -4.46 |  2.53 | 33.47 |      -2.40 |       |
| Car        |      0.00 |        2 | -2.38 |  513.87 | 192.20 |  570.87 | 215.15 |   1.40 |  1.60 |   3.55 |  -4.44 |  2.67 | 46.89 |      -2.47 |       |
| Car        |      0.00 |        2 | -1.70 |  677.08 | 196.47 |  732.16 | 236.22 |   1.36 |  1.63 |   4.02 |   3.64 |  2.35 | 28.57 |      -1.57 |       |
| Car        |      0.00 |        2 | -1.56 |  583.50 | 192.47 |  625.83 | 232.63 |   1.52 |  1.67 |   3.61 |  -0.23 |  2.38 | 30.44 |      -1.56 |       |
| Car        |      0.00 |        2 |  1.99 |  299.69 | 190.81 |  366.89 | 221.46 |   1.47 |  1.77 |   4.25 | -14.75 |  2.48 | 38.64 |       1.63 |       |
| DontCare   |        -1 |       -1 |   -10 |  553.31 | 181.27 |  587.73 | 200.06 |     -1 |    -1 |     -1 |  -1000 | -1000 | -1000 |        -10 |       |
| DontCare   |        -1 |       -1 |   -10 |  624.15 | 180.23 |  687.73 | 202.15 |     -1 |    -1 |     -1 |  -1000 | -1000 | -1000 |        -10 |       |



#### Quick sampling of other images:
- 177 - Car and pedestrians/bikers
- 206 - Car and pedestrians
- 217 - Car and bikers
- 254 - Car and bikers
- 266 - Car and bikers
- 274 - Car and pedestrians/bikers
