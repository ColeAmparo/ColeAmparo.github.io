How does it work?
-----------------

The game itself if very simple, you are allowed to draw a line that the
ball bounces off of, and when the ball touches the green square you win.
Trivial. However I wanted to apply trigonometric concepts I was learning
into this program, so I will tell you how I did it.

Setting up the collision
------------------------

The language I was coding on was not that complex, so it didn’t have a
circle object, but I wanted to make a circle anyways. It did turn out
that you can make as many rectangles as you wanted! But only the top
left coordinate of the rectangle could detect collision. However, if we
had 360 squares, and the top left coordinate of a square could be one
degree of a circle, maybe we can have a circle with collision!

    for(var theta = 0; theta < 2 * pi; theta += pi/180){
        ballR = new Rectangle(2*radiusBall*Math.cos(theta), 2*radiusBall*Math.sin(theta));
        ballR.setPosition(ball.getX()-radiusBall*Math.cos(theta), ball.getY()- radiusBall*Math.sin(theta));
        ballR.setColor(Color.BLUE);

To explain how it works, there is a var theta, which in this case stands
for what degree of the circle we are on. The for loop should iterate 360
times, each time creating a new rectangle with the top left coordinate
(of the rectangle) being the degree of the circle the loop is on. It is
pretty confusing and there is a major oversight as well.

Is it worth the pain?
---------------------

The program doesn’t work perfectly because to detect collision it checks
if the coordinate is above or below the slope of the line created, since
the circle is NOT actually a circle, it has it’s own for loop that
checks each rectangle as the circle object is moving. I did try a
version where very time the circle object moves, all 360 rectangles are
checked before the circle moves again. So I learned that there are
always different solutions to a problem (i.e, not having a circle
object) but sometimes these solutions are not worth implementing… Doing
this did help me understand trig better though.

Try out the code yourself:
[Here](https://codehs.com/sandbox/id/line-game-OJKRwO).
