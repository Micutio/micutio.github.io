---
layout: post
title:  Sharing Saturday September 21
description: Sharing Saturday post on r/roguelikedev
---

After two Saturdays of absence I'm getting back to work on the project. This time I'm having a look at the world generator which still runs the vintage "Rogue"-style level generation from the tutorial. This ought to change. Previously I only ever experimented with cellular automaton-based world generation, which mainly works by 'seeding' the world cells with randomly distributed stats and then 'growing' the world organically using a couple cycles of the automaton. This should work for organ and tissue-like levels, as Innit requires them, as well. However to look for viable alternative and also to expand my own knowledge I'm gonna have a look at Perlin noise and similar techniques.

To make all this more fun and easier to analyze I implemented a debugger that allows to watch the world generation live.

[comments on reddit](https://www.reddit.com/r/roguelikedev/comments/d737v2/sharing_saturday_277/)