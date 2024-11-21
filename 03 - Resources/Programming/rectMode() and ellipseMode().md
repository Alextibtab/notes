---
Resource: Programming
Language: JavaScript
Course: https://timrodenbroeker.de/courses/essentials/
tags:
  - generative_programming
  - programming
  - javascript
---
# Topic / Title: rectMode() and ellipseMode()

2023-01-07
04:17


# Notes
Rectangles and ellipses vary in the way they get positioned on the canvas: Ellipses initially align centered, but rectangles get aligned in the top left corner of the position you set.

This behaviour can be changed with the `rectMode()` and `ellipseMode()` functions

```javascript
// This is the standard 
rectMode(CORNER); 
ellipseMode(CENTER); 

// Center the shape 
rectMode(CENTER); 
ellipseMode(CENTER); 

// Align the shape at the top-left corner 
rectMode(CORNER); 
ellipseMode(CORNER);
```
# Keywords/Questions
`rectMode()`
`ellipseMode()`
# Summary
How to change how shapes are drawn.