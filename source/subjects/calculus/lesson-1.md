# Lesson 1: Rates of Change

~

The universe is full of change.  The universe changes as time passes, and it also changes from place to place.  This is universal to the human experience... the sun rises and sets, the wind blows, rivers flow, and flowers blossom and fade.  Clearly, nature has a tendency to change.  One of the most powerful tools in our human understanding of the physical universe is _calculus_, the mathematics of change.  With calculus, we can describe exactly how things change in time and space, and relate those changes to one another.

## Going for a Walk

To begin our journey into calculus, let's go for a little walk.  As we walk, we move through space... in other words, our position changes.  Imagine that, after walking for \( t \) hours, we are \( 2t \) miles away from home.  Our position is changing, but how fast?

If we travel for 1 hour, we go 2 miles.  If we travel for 2 hours, we go 4 miles.  Clearly, we must be walking at _2 miles per hour_.  Though we may not see it yet, this simple reasoning is critical to the logic behind calculus.  We've calculated the _rate of change_ of our position; in other words, we've calculated our velocity!  Let's extend this reasoning to a slightly more complicated case.

## Dropping the Ball

During our walk, we'll take a brief pause where I pull out a bouncy ball.  I hold the ball at 1 meter from the ground and let go.  The height of the ball can be approximated by

\[ h(t) = 1 - 5 t^2 \]

where \( h \) is the height of the ball (in meters) and \( t \) is the time since I let go of the ball (in seconds).  One tenth of a second after I let go of the ball, how fast is it going?

This is a more difficult question to answer.  In our experience, when we drop a ball, it seems to get faster as it falls.  How can we know its velocity at a single point in time?  We calculate velocity as \( v = d / t \), where \( d \) is the distance traveled and \( t \) is the time elapsed.  But at a _single point in time_, no time elapses, and the ball doesn't move, so we have \( v = 0/0 \) which is indeterminate!  So what shall we do?

## A Stroke of Genius

After some thinking, you have a brilliant idea.  What if, instead of finding the velocity at a single point in time, we calculate it for a very short duration of time?  Surely that will give us an answer that's good enough.  So you try this between two points in time: \( t = 0.1 \, \mathrm{s} \) and \( t + \Delta t = 0.2 \, \mathrm{s} \).  Here, we're using the symbol \( \Delta t \) to indicate a very short duration of time, which is currently one tenth of a second.

\[ \begin{align*} h(t) &= 1 - 5 \cdot (0.1)^2 = 1 - 0.05 = 0.95 \\ h(t + \Delta t) &= 1 - 5 \cdot (0.2)^2 = 1 - 0.2 = 0.8 \\ \end{align*} \]

This leaves you to conclude that the velocity of the ball is _approximately_

\[ \begin{align*} v &\approx \frac{h(t + \Delta t) - h(t)}{\Delta t} \\ &= \frac{0.8 - 0.95}{0.1} = -1.5 \, \mathrm{m/s} . \end{align*} \]

But you know that this is only an average velocity between \( t = 0.1 \, \mathrm{s} \) and \( t + \Delta t = 0.2 \, \mathrm{s} \).  To get something more accurate, you change \( \Delta t \, \mathrm{s} \) to a smaller value.  Let's use one hundredth of a second.

\[ \begin{align*} h(t) &= 1 - 5 \cdot (0.1)^2 = 1 - 0.05 = 0.95 \\ h(t + \Delta t) &= 1 - 5 \cdot (0.11)^2 = 1 - 0.0605 = 0.9395 \\ \end{align*} \]

\[ \begin{align*} v &\approx \frac{h(t + \Delta t) - h(t)}{\Delta t} \\ &= \frac{0.9395 - 0.95}{0.01} = -1.05 \, \mathrm{m/s} . \end{align*} \]

Very interesting... the average velocity of the ball is very close to \( -1 \, \mathrm{m/s} \) now.  But this is still just an approximation of the _instantaneous_ velocity... the velocity that occurs _exactly_ at \( t = 0.1 \, \mathrm{s} \).  You wonder if you could somehow make \( \Delta t \) shorter and shorter (but never quite zero!) you would get closer and closer to an exact answer.  To do this, we'll need some new mathematical tools...

[Next Lesson](lesson-2)