# Topic / Title: Styling Shapes with Stroke and Fill

2023-01-07
04:05


# Notes
By default any shapes drawn will have a stroke of 1 pixel width and be filled in gray. To modify this behaviour there are the following functions:
- `stroke()`
- `noStroke()`
- `strokeWeight()`
- `fill()`
- `noFill()`

The `stroke()` function lets you define the colour of the outline of your shape, whereas `noStroke()` will turn off the outline
```javascript
stroke(0); // set the stroke colour to black
noStroke(); // deactivate the stroke
```

`fill()` and `noFill()` work exactly the same way but affect the fill-colour of the shape instead.
```javascript
fill(0); // set the fill colour to black
noFill(); // deactivate the stroke
```

`strokeWeight()` defines the thickness of the outline in pixels.
```javascript
strokeWeight(50); // a very thick stroke
```

These functions will only affect the shape if executed before drawing the shape so these functions should be called before drawing shapes

# Keywords/Questions
`stroke()`
`noStroke()`
`strokeWeight()`
`fill()`
`noFill()`

# Summary
How to style shapes

Related: [[essentials course]]
Tags: #generativeProgramming #timrodenbroeker 
