---
layout: post
title: "A Simple Exercise to Understand the Prediction-Making Conducted by Machines"
date:   2019-01-19 12:00:00 -0800

---
In school, after we learn that a line is made by connecting two points, after we learn how to draw such a line into a 2D Cartesian graph, and after we learn that such a graph has an *x* axis that extends from left to right and a *y* axis that extends from top to bottom, we also learn that the slope of a line can be calculated with the following formula...

`y = mx + b`

...where points x and y form a coordinate (x,y) on the graph, the variable *m* represents the slope of a line between that point and another, and the variable *b* is the exact point at which the line made from those two points crosses the vertical y-axis of the graph.

We also learn that a positive slope (+m) gives us a line that inclines upwards from left to right on a graph and that a negative slope (-m) gives us a line that declines downwards from left to right.

This equation is helpful, because if you learn of two points (x<sub>1</sub>,y<sub>1</sub>) and (x<sub>2</sub>,y<sub>2</sub>), you can draw a line between them, and from that line, you can do three things:

1. you can extrapolate where the line will cross the y-axis, thereby determining the value of *b*,
2. you can, with variables *x*, *y*, and *b* and a pencil in hand, use the above formula to calculate your slope *m*, and
3. you can make a prediction about what other values (x<sub>?</sub>,y<sub>?</sub>) might fall on the same line

This is what very basic _linear regression_ is (with data that falls on or very near that line).

## A Curious Example
If you could put a value on curiosity, and **if** curiosity increased linearly and remained consistent over a lifetime, and if I told you that when I was five years old, I had a curiosity of 10, and that by age 20 I had a curiosity of 40, you could of course predict that by the age of 50, I'll have a curiosity of 100:

- (x<sub>1</sub>,y<sub>1</sub>) = (5,10)
- (x<sub>2</sub>,y<sub>2</sub>) = (20, 40)
- y = mx + b, thus we have
- 10 = m(5) + 0 <~ (we extrapolate, and know from common sense, that at age zero, my curiosity would have been 0, thus this is the y-intercept)
- From this and using our equation, we can solve for *m* by dividing 10 by 5, and we find that m = 2

We've just calculated that my curiosity increases by 2 every year of my life, and from that, we can go on to predict that if my curiosity at age 20 was 40, then thirty years later, when I turn 50, my curiosity will have increased by another 60 points, thus we predict that my curiosity at age 50 will be 100.

What we teach learning machines to do is to take data, often significantly more complex data than what I've provided above, and use math to first fit the data to a line or a curve and then, analogously to what we just did, use that line or that curve to make predictions. At least, that's my current understanding of what training a learning machine on data partially involves. There also appear to be many different types of linear, curvilinear, and non-linear regression, as well as many analyses that are not regression-based.

As with all things machine learning, the types of math involved, the statistical analyses used, the types and formats of training data selected, and the architectures and numbers of artificial neural networks employed all change depending on the sort of predictions that need to be made.

But math, just as in our brains, is at the heart of all this curious prediction-making machine learning software is making.

## Further Reading
[1] https://en.wikipedia.org/wiki/Cartesian_coordinate_system

[2] https://en.wikipedia.org/wiki/Linear_regression

[3] http://www.stat.yale.edu/Courses/1997-98/101/linreg.htm
