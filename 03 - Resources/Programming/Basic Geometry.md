---
Resource: Programming
Language: JavaScript
Course: https://timrodenbroeker.de/courses/essentials/
tags:
  - programming
  - generative_programming
  - javascript
---
# Topic / Title: Basic Geometry 

2023-01-07
03:57


# Notes
Two new functions `rect()` and `ellipse()` which both take four arguments
the first two are an X, Y coordinate where the shape should be drawn then the last two parameters are for how big the shape should be.
```javascript
function setup() {
  createCanvas(500, 500);
}

function draw() {
  background(220);
  ellipse(mouseX, mouseY, 100, 100);
}
```
Also some new keywords: `mouseX`, `mouseY` these are handy variables P5js provides the user which will track where the users mouse position is. In the code above we use these variables in the `ellipse()` function so now the circle will follow the mouse
# Keywords/Questions
`rect()`
`ellipse()`
`mouseX`
`mouseY`
# Summary
Basic functions for drawing shapes are `rect()` and `ellipse()`