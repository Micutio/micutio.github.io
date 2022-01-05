---
layout: post
title:  Sharing Saturday November 28
description: Sharing Saturday post on r/roguelikedev
---

Last week I started migrating Innit from tcod to bracket-lib and today the transition is complete. I've learned a lot while perusing the tutorial code and , for example, slimmed down the input processing drastically.

There was a very insightful discussion about UI/UX and accessibility, particularly mouse controls [here](https://www.reddit.com/r/roguelikedev/comments/jkb6pz/a_request_from_someone_whod_like_to_get_more_into/gajcmti/) which prompted me to support this as well.
Since neither tcod nor bracket-lib have support for mouse-interactable ui elements I went and rolled my own little system, which was surprisingly easy.

Another crucial element the needs to be customised is the game loop. Since the game is taking place inside a living organism, Innit's core tenet is that everything in the game is made out of living cells.
That means there are a ton of individual objects to update at every turn, currently 4800 in the standard 80x60 world size. The default game loop structure of bracket-lib, if I understood it correctly, is too slow for that because there is too much happening in between each object update. My own loop updates the objects in batches and renders only if there have been any effects visible to the player. This turns the turn times from minutes back into milliseconds and increases the fps by an order of magnitude.

So all in all, adding viruses, migration to bracket-lib, full mouse control and the pending UI re-design will soon be tied up into another major alpha release.

On personal note, recently I'm feeling an urge to speed up the development of this game. Innit is the first hobby project of mine that I feel comfortable sharing and that other people might be interested in. This is why I'm putting in the effort to increase accessibility. Once Innit reaches the state of a presentable concept demo I want to create a website/dev blog for it and start sharing it on my social media.

[comments on reddit](https://www.reddit.com/r/roguelikedev/comments/k2cpce/sharing_saturday_339/)
