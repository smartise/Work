---
Done: false
"date:":
tipe: Methodologysub
tags:
---
based on article [[zawadaQuantifyingCoralMorphology2019]].
# Shape  variable 
## Volume compactness
volume compactness is calculated by two variable sphericity and convexity. 
### Sphericity 
This variable calculate how close an object's shape is to a sphere. 
it is size invariant
it is calculated as the ratio of the surface area of a sphere with the same volume as the object and the surface area of the object. 
$$
S = \frac{\text{Surface sphere}}{\text{Surface object}}
$$
### Convexity 
convexity is a size invariant measure of the degree to which there is space between different parts of an object 

it is calculated as the volume of an object divided by the volume of its convex hull, where the convex hull is the shape formed by the smallest possible boundary that has no concave areas around an object
$$
C = \frac{\text{Volume object}}{\text{Volume convex hull}}
$$
## Surface complexity 
surface complexity is calculated by two variable : packing and fractal dimension 
### Packing 
packing (P) is a size invariant ratio of how much object's surface area is situated internally versus externally in relation to its immediate environment. 
it is calculated as the surface area of an object divided by the surface area of the convex hull. 

$$
S = \frac{\text{Surface object}}{\text{Surface convex hull}}
$$

#qst on est bien daccord que cette variable ne peut pas dépasser 1 (contrairement dit dans l'article)
### Fractal Dimension 
Fractal dimension (D) capture how surface area fills space and is an estimate of spacial complexity. 

The fractal dimension is based on the cube counting algorithm: 

The cube counting algorithm is a method used to estimate the fractal dimension of a three-dimensional object. It's a 3D analogue of the well-known 2D "box counting" method used for two-dimensional fractals. Here's a basic overview of how it works:

1. **Grid Overlay**: Begin by overlaying the 3D object with a grid of cubes (or boxes) of a specific size.
    
2. **Counting**: Count the number of cubes that contain a part of the object.
    
3. **Resizing and Repeating**: Reduce the size of the cubes and repeat the process, counting the number of smaller cubes that contain a part of the object.
    
4. **Log-Log Plot**: Plot the logarithm of the number of cubes against the logarithm of the size of the cubes.
    
5. **Slope Calculation**: The slope of the line obtained in the log-log plot gives an estimate of the fractal dimension of the object.

fractal dimension is calculated as the slope of log_10(N)~log_10(C) where N is the total number of cubes that contain any surface of the object and C is the number of equal sized cubes in the 3D cube array. 

$$D = \frac{\log(N(\epsilon))}{\log\left(\frac{1}{\epsilon}\right)}
$$

![[slope fractal dimension.png]]
got from [[sarkarEfficientDifferentialBoxcounting1994]]
where : 
- N is the number of boxes and epsilon the size of the boxes
- D is the fractal dimension aka the slope of the graph 
- C is a constant 
## top Heaviness
top heaviness was capture by the first moments of volume ($V_{vol}$) and the surface area ($V_{Area}$) with respect to the vertical distance from the attachement area.  

to ensure size invariance, both variables has to be $log_{10}$ transformed. 
### First moment of volume 
the first moments of volume is calculated by multiplying the volume of each tetrahedron in the mesh multiplied by the vertical distance from the centroid of the triangle (the center of the triangle) and the centroid of the attachment plane (point of attachement of the coral)

$$VVOL = \sum V_{\text{tetra}} \times \text{Vertical distance}
$$
### Aera and volume 
For the surface area ($V_{Area}$) the area of each triangle in the mesh was calculated and multiplied by the vertical distance from the centroid of the centroid of the triangle and the centroid of the attachment plane 

$$VAREA = \sum A_\text{triangle} \times \text{Vertical distance}
$$


