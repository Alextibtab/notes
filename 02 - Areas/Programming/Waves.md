---
Area: Programming
Language: JavaScript
Course: https://timrodenbroeker.de/courses/essentials/
tags:
  - programming
  - generative_programming
  - javascript
---
# Topic / Title: Waves

2023-01-08
22:08


# Notes
wave functions such as `sin()` and `tan()` can be utilised for many different functions. They can be used for animating objects.

Examples:
- Ellipse moving across screen in sine wave motion
```javascript
function setup() {
  createCanvas(600, 400);
}

function draw() {
  background(0);
  ellipseMode(CENTER);
  translate(0, height / 2);
  ellipse((frameCount * 5) % width, sin(radians(frameCount % width) * 5) * 100, 20);
}
```


# Keywords/Questions
`sin()`
`tan()`
# Summary