---
Area: Programming
Language: JavaScript
Course: https://timrodenbroeker.de/courses/essentials/
tags:
  - generative_programming
  - programming
  - javascript
---
# Topic / Title: Geometric Typography

2023-01-08
20:49


# Notes
This is an exercise to create some typographic characters using processing 

# Keywords/Questions
Exercise brief:
- Design 3-5 typographic characters
- implement using processing
- only black and white for colours
# Summary
```javascript
function setup() {
  createCanvas(600, 400);
}

 

function draw() {
  let letterHeight = 100
  const baseline = (height / 2) + (letterHeight / 2)
  
  background(0);
  stroke(255);
  
  // A
  strokeWeight(10);
  strokeCap(SQUARE);
  line(80, baseline, 120, baseline - letterHeight);
  
  strokeWeight(5);
  strokeCap(ROUND);
  line(160, baseline, 125, baseline - letterHeight + 5);
  
  strokeWeight(8);
  line(110, baseline - 40, 135, baseline - 40);

  // L
  strokeWeight(10);
  strokeCap(SQUARE);
  line(200, baseline - 10, 200, baseline - letterHeight);  
  
  strokeCap(ROUND);
  strokeWeight(5);
  line(198, baseline, 250, baseline);
  
  // E
  strokeWeight(10);
  strokeCap(SQUARE);
  line(290, baseline - 10, 290, baseline - letterHeight + 10);
  
  strokeWeight(5);
  strokeCap(ROUND);
  line(288, baseline, 350, baseline);
  line(288, baseline - letterHeight, 350, baseline - letterHeight);
  
  strokeWeight(7);
  line(305, baseline - letterHeight / 2, 325, baseline - letterHeight / 2);
  
  // X
  strokeWeight(10);
  strokeCap(SQUARE);
  line(390, baseline - letterHeight, 460, baseline);

  strokeCap(ROUND);
  strokeWeight(5);
  line(390, baseline, 425 - 10, baseline - letterHeight / 2 + 10);
  line(460, baseline - letterHeight, 425 + 10, baseline - letterHeight / 2 - 10);

}
```
![[geometricTypography.png]]