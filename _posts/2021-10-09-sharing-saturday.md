---
layout: post
title:  Sharing Saturday October 09
description: Sharing Saturday post on r/roguelikedev
---

Finally another update after two months of radio silence. The good news is that I checked off all the items from the road map laid out in the previous Sharing Saturday post:

_Switching world generation to the dedicated cellular automaton (CA) library_

This makes creating and stepping the world generation CA much more ergonomic, development wise, than the hacked-together generator previously used by Innit. I also learned a bunch about creating, testing and benchmarking libraries in Rust. Overall nice experience and the game will be better for it.

_Improved world generation_

After the improved CA implementation I perused http://www.netlogoweb.org/launch, which is a really nice online library of simulation models, for suitable CA strategies to generate organic-looking worlds. Out of several shortlisted models I found that one based on forest fire propagation yields the best-looking results for now.

_Cell reproduction and growth gradient_

The output of the world generation CA is a morphogen value for each tile of the world.

Wikipedia:
> Typically, morphogens are produced by source cells and diffuse through surrounding tissues in an embryo during early development, such that concentration gradients are set up. These gradients drive the process of differentiation of unspecialised stem cells into different cell types, ultimately forming all the tissues and organs of the body.

In the case of Innit we use the gradient simply to determine where wall cells can grow and where not. During wall cell reproduction that morphogen concentration is used as the probability of placing a new wall tile at a given position. So whenever a wall cell performs cell division and places an offspring wall cell the world can slightly change its appearance, but still maintain the general layout. This is bringing us a big step forward in making the world around the player feel like a living organism.

As a nice by-product of the development effort, Innit's debug mode has been enriched with two more neat features. Now debug mode can visualise the world generation and also support a pectator mode to allow the game to run without a human player. Both of these features have been added to allow viewing and debugging the world generation and cell life and reproductive cycle.

_Summary_

The first clip shows the old world generation that was the naive CA hack with a slightly randomised carving out of a cave.

[old world generation, fairly boring cave](https://imgur.com/shMxZ0O)

The second clip shows the improved world generation and spectator mode, viewing a sped-up change of the environment over time, effected by dying and regenerating wall 'tissue' cells.

[new world generation, based on forest file propagation and slightly changing shape over time](https://imgur.com/uQ0JHB6)

Only disadvantage of the new CA is that it's harder to get consistent world sizes. There is a low chance of comically small worlds if the forest-fire-like propagation of growth gradients fizzles out way too early. But hey, it's a start and it'll be interesting to play around with more CA rules and try to come up with some by myself.

[comments on reddit](https://www.reddit.com/r/roguelikedev/comments/q4a26h/sharing_saturday_383/)
