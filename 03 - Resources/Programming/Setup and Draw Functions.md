---
Resource: Programming
Language: JavaScript
Course: https://timrodenbroeker.de/courses/essentials/
tags:
  - generative_programming
  - programming
  - javascript
---
# Topic / Title: Setup and Draw

2023-01-07
03:39


# Notes
The foundation of any Processing or P5.js sketch is based on two functions: `setup()` and `draw()`. In short, `setup()` defines the project-details whereas `draw()` defines what happens over time

```javascript
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
}
```
The above javascript code is the default code provided when creating a new sketch in P5.js

#### Setup
first inside the setup function the `createCanvas()` function takes two parameters which will represent the width and height of the sketch. 

#### Draw
Once the `setup()` function has been called by the computer then the `draw()` loop will run any code inside this function will repeatedly be executed until the program is stopped.

Currently, all the `draw()` function is doing is setting the background colour using the `background()` function which takes either a singular value which will then be used for the RGB components of the colour or you could pass in three parameters to customise each RGB value
```javascript
background(50, 100, 150);
```
Also note because this is inside the `draw()` function the screen is repeatedly being coloured in each time `draw()` is called this is useful if we're updating the positions of objects that move inside the sketch if we didn't first clear the background then the objects would appear to smear across the screen. 

ps. background can take RGBA parameters as well to specify transparency
# Keywords/Questions
`setup()`
`draw()`
`createCanvas()`
`background()`

# Summary
Every P5.js has the same base structure a `setup()` function that is initially ran to configure the sketch and then a `draw()` function which will keep being called until the program is suspended.