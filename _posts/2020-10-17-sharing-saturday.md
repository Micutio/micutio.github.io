---
layout: post
title:  Sharing Saturday October 17
description: Sharing Saturday post on r/roguelikedev
---

The three weeks since the last update have been important to get development unstuck and fun again. The main goal was to implement a random AI to breathe some more life into the game after the turn-passing AI quickly reached the limits of its usefulness.
The new AI will execute random actions with a random target, if it can find a combination of both that is valid.

Getting there led me to revamp the action and genetics system and input processing substantially. While the concept was and is still sound in my mind, the implementation of it was too convoluted and adding new content required touching too many components. With a whole year between me and my old self there was easily enough emotional distance to cut down the over-engineered wild growth and tighten up the code.

Meanwhile, plenty of testing has helped me find and fix plenty of bugs. And _finally_ the rate of checking for user input is now limited to avoid checking every other nanosecond and eating the CPU alive.

To celebrate getting rid of this roadblock the game received a little symbolic release of version 0.0.2!

Next I'm going to add a couple new genetic traits to spice up the entity DNA generation and in the same vein create a simple form of metabolism and energy costs for actions. Finally a little more adding content and a little less working on the engine in sight.

[comments on reddit](https://www.reddit.com/r/roguelikedev/comments/jcl40q/sharing_saturday_333/)