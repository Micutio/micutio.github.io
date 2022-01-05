---
layout: post
title:  Sharing Saturday January 1
description: Sharing Saturday post on r/roguelikedev
---

After over a year of slow but steady development it is way past time for another version bump. Innit alpha 0.0.5 is here.
This is a special one because I finally feel comfortable enough to call it a playable alpha.
The entire infrastructure is now there, complete with main menu, game loop and lose/win screen.
All known game-breaking bugs and major performance sinks have been fixed to allow for uninterrupted gameplay.

So let's have a look at the most significant improvements:

**Fundamental world overhaul**

The entire game layout has been changed to better reflect the nature of the game.

Main menu: [before](https://imgur.com/6mpUZWt) and [after](https://imgur.com/6V62fbs)

Game interface: [before](https://imgur.com/uj9xK8f) and [after](https://imgur.com/1KCxGNP)

This is motivated by aesthetic and narrative reasons.
As the game takes place inside of the human body I want the game interface to look like a medical device to create immersion for the user and somewhat convey an atmosphere of high stakes. Additionally the narration will take place as a dialog between doctors and scientists whom are observing the player cell using the very microscope represented by the UI.

Initially I wasn't sure whether the player would be one of the scientists/doctor or the cell itself, but I settled on the latter.
A scientist/doctor steering a singular cell would be too immersion breaking and also hard to reconcile with future game mechanics along the line of steering multiple cells and permadeath. The cells will live and die, but the external human observers remain a constant.
It's much more interesting to have this element in the game of being watched and commentated on.

Something I'm not quite certain on is the world visibility. Whereas in the old version the world was completely black initially and had to be explored, it is now explored from the start but still with a limited field of view. The former wouldn't make sense when combined with the microscope UI redesign but I'm still hesitant as to whether I should remove the fog of war altogether. It feels like it still makes sense to keep it to have a certain degree of uncertainty and exploration.

**Compiling to wasm, embedding in web page**

This one is a major milestone in terms of accessibility and was one of the main reasons to switch to bracket-lib.
For those unfamiliar, compiling to wasm (or WebAssembly in long) allows the game to be embedded in a website and be played like any other javascript-based webgame.
Pointing to website will make it so so much easier to get interested people to try out the game than having to download and install it first.
Granted the web version will lack a few features like saving the game and modding data files, but for now there is hardly any difference.

The web version of Innit can now be played here: https://micutio.github.io/innit/

[comments on reddit](https://www.reddit.com/r/roguelikedev/comments/rt6kqf/sharing_saturday_395/)
