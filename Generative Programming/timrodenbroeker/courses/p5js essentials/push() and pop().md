# Topic / Title: push() and pop()

2023-01-08
21:46


# Notes
By default any transformations will affect the global matrix/coorindate system which can make transforming individual shapes hard/impossible as all transformations will compound on one another by default. To get around this there are the `push()` and `pop()` functions which will apply transformations on their own matrix/coordinate system.

First you write `push()` which will let processing know that any following transformations should be applied to their own matrix then at the end you put `pop()` once the transformations have been applied.

Example sketch of two rectangles rotating around the centre in opposite directions
```javascript
void setup() {
	size(900, 900);
}

void draw() {
	background(#f1f1f1);
	fill(0);
	noStroke();
	rectMode(CENTER);

	push();
	translate(width/2, height/2);
	rotate(radians(frameCount));
	rect(0, 0, 50, 700);
	pop();

	fill(#aaaaaa);
	push();
	translate(width/2, height/2);
	rotate(radians(-frameCount));
	rect(0, 0, 50, 700);
	pop();
}
```

# Keywords/Questions
`push()`
`pop()`
# Summary
How to apply transformations to objects invdividually/grouped instead of globally

Related: [[essentials course]]
Tags: #generativeProgramming #timrodenbroeker 