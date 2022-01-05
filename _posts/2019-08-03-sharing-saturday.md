---
layout: post
title:  Sharing Saturday August 03
description: Sharing Saturday post on r/roguelikedev
---

Not quite as much progress as I hoped. Ironically it was not the DNA implementation directly that caused head scratching, but rather the input processing. Any player action has parameters that originate from it's DNA and control the range, energy cost etc. of the action. Then during the game, actions require another parameter which depends on the current game state, e.g. a target object, target id or direction. Both of these parameter sets have to be put together to create the action instance. Which also means that both of these have to have a mapping to the same action, so that we know where to get and where to apply the parameters. And all of this has to be bound to keys or mouse buttons, in the future ideally via config file.

It's overall not too hard to make this happen, but it gets tougher if we want to minimize the number of code edits to add new actions and parameters as well as keep player input and gameplay decoupled.

Researching design patterns and implementing a workable input handling is what most of my week went into. Nothing to write home about really, it still feels messy but it'll do for the time being.

To give you something for the eyes, I also played around with color schemes for a [light](https://github.com/Micutio/innit/blob/input-revamp/screenshots/innit_light_theme.png) and [dark](https://github.com/Micutio/innit/blob/input-revamp/screenshots/innit_dark_theme.png) mode. It's a little annoying how much better the dark mode seems to have turned out. After all light mode is supposed to be the default but something is still a little off.

Anyways, that's just on the side sidelines. DNA generation and parsing is still in the works and should have the first playable prototypes in the next couple days.

[comments on reddit](https://www.reddit.com/r/roguelikedev/comments/clbxlf/sharing_saturday_270/)