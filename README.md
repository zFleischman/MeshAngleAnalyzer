# MeshAngleAnalyzer
Determines whether or not a manifold (i.e. watertight) mesh has any sharp edges.

Run `find_sharp_edges.py` and pass it a triangle mesh in an **.stl** file format.
By default it will test for edges of 80 degrees or less.

## Dependencies
- numpy-stl
- matplotlib

## Usage
```
usage: find_sharp_edges.py [-h] [-t THRESHOLD] [-v] STL_FILE

Analyze a manifold mesh to see if it has acute edges. Display offending edges.

positional arguments:
  STL_FILE

optional arguments:
  -h, --help            show this help message and exit
  -t THRESHOLD, --threshold THRESHOLD
                        The degree in angles that all edges must be greater
                        than (default=80 degrees, max=89 degrees)
  -v, --view            Show a plot of the model instead of analyzing it.
```

## Visualization
If there are edges that are too sharp, they will be automatically visualized as such:
![alt tag](https://github.com/zFleischman/MeshAngleAnalyzer/blob/master/sharp_heart.png)
![alt tag](https://github.com/zFleischman/MeshAngleAnalyzer/blob/master/star.png)

To simply see the model in all it's glory, pass the **-v** flag:
![alt tag](https://github.com/zFleischman/MeshAngleAnalyzer/blob/master/heart_mesh.png)

