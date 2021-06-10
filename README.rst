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

General
=========

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
browser/system.

Once over allow double click on canvas to start a fresh game.


Odd behavior in some devices
==============================

Offscreen canvas (Exp)
------------------------

Try offscreen canvas for background (plain color + once in a while zones) to see,
if the very odd toomuch out of sync AnimFrame timing seen in one mobile, as well
as the inconsistency in ipad (but still visually smooth enough) changes or not.

   Avoid translucent background fill related motion effect for now.

   Not only ignore/drop too large delays wrt anim frames (say when user switches
   back and forth with some other app or browser tab or so), but also control
   the logical frame matching wrt skipped frames (due to missing call back), to
   be within a max of 1+1 dropped frame.


setInterval (ExpSI)
----------------------

Reverting to setInterval from requestAnimationFrame to see, if the odd behavior
wrt timing btw frames noticed on a specific mobile and also the jittery but
visually fine behavior noticed on iPad, changes with this or not.

The setInterval based logic seems to be more consistent (not necessarily perfect
or fully smooth, but still) on the mobile which had the very inconsistent timing,
however do note that it also by default aims for only 25 fps (based on my setup),
compared to the ideal 60 fps aimed for animFrames by browser. Need to cross check
this once again later and explore further later.

