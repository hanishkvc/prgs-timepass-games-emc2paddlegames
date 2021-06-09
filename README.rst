###################################
Browsers, Javascript, Canvas, ...
###################################
Author: HanishKVC
Version: v20210606IST0224


Overview
###########

A simple paddle game to test out the canvas in browsers using javascript. It is a
game of a bit of luck and equally a bit of gamer control.

Also as a thank you to few kids for helping out with making delicious pizzas,
as well as as a crude example to allow them to replicate and or expand and or ...
using their own logics, mechanisms, imagination, ... in their own environments be
it scratch or pygame or swift or browser-javascript or ...

And to provide some time pass, once in a bluemoon.

One can run this on a desktop/laptop by going to

https://hanishkvc.github.io/prgs-timepass-games-emc2paddlegames/browser/

The index.html itself contains the ui and the logic.


Misc
#######

Show level, points, time taken to make it interesting in a way.

   Adjust points with level.

   Accelerate with level.

   Random special zones to gain more points or slow down.

      Give reason for user to move around and or look forward to.

   User decides whether to switch levels or not.

Adjusts canvas to device display size to some extent. Same with the font used.

Paddle movement adapts to distance from ball and direction of motion requested,
thus making it relatively easy to control on a mobile/tablet by tapping on screen.

Trap double tap zoom on mobile/tablet devices wrt the game canvas, so that user
can tap and control the game.

Randomly place ball and paddle at beginning.

Allow ball to warp around the screen horizontal boundries, but not the paddle.

Random random everywhere to make the repeat place less predictable.

Use math to hopefully control the acceleration/deceleration curves.

If user enters a standard repeat pattern then jostle them out of it, by changing
level and direction of deflection.

Use callback time of requestAnimFrames, to try and sustain a uniform animation/game
speed effect across devices/systems/browsers.

Simulate a feel of movement by using partially transparent clearing of the frames.

Use text shadows to make it visible even if contrast between text and background
is less.

Alert user if there is too much variation between animation frame calls from the
browser.

