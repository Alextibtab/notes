# Topic / Title: Lines, Triangles and Polygons

2023-01-08
20:30


# Notes
`line()` This function is used to draw lines the function takes 4 parameters for the two different points to plot the line between.
```javascript
line(x1, y1, x2, y2);
```
`triangle()` This function is used to draw a triangle and takes 6 parameters for the 3 points that will be connected into a triangle
```javascript
triangle(x1, y1, x2, y2, x3, y3);
```

To draw more complex shapes there is the following functions `beginShape()`, `vertex()`, `endShape()` To start drawing a shape use the `beginShape()` function to tell processing you want to start drawing a shape then use the `vertex(x1, y1)` function for each point you want to create then when finished adding the vertexes use `endShape()`. There is also `curveVertex()` which will draw smooth lines between points instead of straight lines.
# Keywords/Questions
`line()`
`triangle()`
`beginShape()`
`vertex()`
`curveVertex()`
`endShape()`
# Summary
How to draw lines, triangles and custom complex shapes.

Related:  [[essentials course]] 
Tags: #generativeProgramming #timrodenbroeker 