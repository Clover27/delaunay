Compute the delaunay triangulation of a set of points.

Currently compute 2D Delaunay triangulation via a divide and conquer algorithm. The overall complexity is of O(n \log n)

The interface is very simple, only one function call is needed to generate the triangulation:

```
int delaunay2d(point_t points[], int num_points, int **faces);
```

points: is the set of input points
num\_points; is the number of points
faces: the faces of the delaunay triangulation. This array contain a sequence of the following elements: each face is preceeded with the number of vertices and then the vertex indices follow e.g. 3, v0, v1, v2, 4, v0, v5, v6, v7, 3, ....
The first face is the external face (i.e. the convex hull)
return the number of faces in the triangulation