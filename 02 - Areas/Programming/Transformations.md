---
Area: Programming
Language: JavaScript
Course: https://timrodenbroeker.de/courses/essentials/
tags:
  - generative_programming
  - programming
  - javascript
---
# Topic / Title: Transformations

2023-01-08
21:36


# Notes
Transformations are used to move, scale and rotate shapes.
To move shapes in P5.js there is the `translate()` function which takes two parameters an X and Y coordinate.
```javascript
translate(x, y);
```

To rotate objects there is the `rotate()` function which takes a single parameter which is the angle the object should be rotated to.
```javascript
rotate(angle);
```

However, the rotate function doesn't use degrees for angles but instead uses radians to convert normal angles into radians there is the `radians()` function which will convert a value into radians.
```javascript
rotate(radians(angle));
```

To resize an object there is the `scale()` function which takes a single parameter which will scale the object by a percentage
```javascript
scale(2.0); // scale object to 200%
scale(0.5); // scale object to 50%
```

# Keywords/Questions
`translate()`
`rotate()`
`radians()`
`scale()`
# Summary
How to move, scale and rotate shapes in processing.