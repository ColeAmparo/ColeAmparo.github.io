---
layout: project
type: project
image: images/trigGame.png
title: Trigonometry Game
permalink: projects/triggame
date: 2018-05-22
labels:
  - Trigonometry
  - Basic Javascript
summary: A game that uses trigonometry to detect collision between a ball and a line.
---


Summary
-----------------

The game itself is very simple, you are allowed to draw a line that the
ball bounces off of, and when the ball touches the green square you win.
Trivial. However I wanted to apply trigonometric concepts I was learning at the time into this program, so I will tell you how I did it.


<img class="ui image" src="{{ site.baseurl }}/images/UnitCircle.png">


### Setting up the collision

The website I was coding on was not that complex, the circle object did not have collision on all sides. It is also possible to make squares but only the top left coordinate of the square could detect collision. However, if we
had 360 squares of the same size, and the top left coordinate of the each square could be one
degree of a circle, maybe we can have a circle with collision! It would be similar to the image above but instead of 3 squares it would be 360.

```
 line 1   for(var theta = 0; theta < 2 * pi; theta += pi/180){
 line 2      ballR = new Rectangle(2*radiusBall*Math.cos(theta), 2*radiusBall*Math.sin(theta));
 line 3      ballR.setPosition(ball.getX()-radiusBall*Math.cos(theta), ball.getY()- radiusBall*Math.sin(theta));
 line 4      ballR.setColor(Color.BLUE);
```

To explain how it works, there is a variable theta, which in this case stands
for what degree of the circle we are on. The for loop iterates 360
times (line 1), since theta is incremented by pi/180 and the loop stops when theta > 2 * pi. In line 2 the size of the rectangle is created, and in line 3 the x and y of the top left of the coordinate are set to degree theta. Line 4 specifies the color.

## Contribution

I made the entire program myself, my Trigonometry and Coding teacher also gave me a lot of advice as I was working on the program.


What I learned
---------------------

The program doesn’t work perfectly because to detect collision it checks
if the coordinate is above or below the slope of the line created. Since
the circle is NOT actually a circle, (it is 360 seperate squares) it has it’s own for loop that
checks each square as the circle object is moving. I did try a
version where every time the circle object moves, all 360 rectangles are
checked before the circle moves again. However, that solution had a horrible runtime and wouldn't work. So I learned that there are
always different solutions to a problem (i.e, not having a circle
object with full collision) but sometimes these solutions are not worth implementing… This project did help me get a better understanding of Trigonometry.

Try out the code for yourself:
[Here](https://codehs.com/sandbox/id/line-game-OJKRwO).


