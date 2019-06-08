# Recursive Loops

I'm going to call loops within loops *Recurrsive Loops* for lack of a better term.


## Issue / Motivation

One of the aspects of NES development that had me stumped for a while was looping through "2d arrays" like the AOM.

I always wrote my code to minimize the number of *recurrsive loops* -- which is almost always a good practice -- but caused a lot of issues for me when dealing with manipulating *sprites* (collection of tiles). I would have to loop through sprites, tiles, and the particular attributes for each tile.


# Solution

I was thinking about designing my own CPU and how I would handle this situation and it hit me. I would allow pushing the *index register* to the stack. Then you can push and pop for each subsequent loop. And that is the exact reason the designers of the MOS 6502 gave the *X register* the ability to push to the stack.

This is probably pretty obvious to people who have programmed assembly on older CPUs or micro-controllers, but I find it so ingeniously simple, and I love figuring this stuff out on my own.
