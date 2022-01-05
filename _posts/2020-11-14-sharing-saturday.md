---
layout: post
title:  Sharing Saturday November 14
description: Sharing Saturday post on r/roguelikedev
---

Me from last week:

> Next week will be all about viruses with a bit more research and hopefully complete first revision of the virus gameplay.

Happy to report this week that the first revision of the virus implementation is close to finished. Innit now has two kinds of viruses: RNA viruses and retroviruses. All a virus does is look for a cell with matching receptors that it can attach to and inject its own RNA/DNA. RNA viruses replace the cell control directly to force them to reproduce the virus either for a couple of turns or until  the cell bursts and dies. Retroviruses insert their DNA into the host cell's. This changes the cell's genetic makeup (for better or worse) and allows for the virus to go dormant and break out periodically. 

Primarily viruses will serve as threats to the player and the host organism in the game. Secondarily the player can also use them to purposefully alter their own genome or engineer a non-threatening virus to attack harmful bacteria or improve the abilities of friendly cells. This is where I hope the combination of procedural generation and emergent behavior will lead to a large space of gameplay options the player can explore to reach their goals.

Next week I'll finalise the virus implementation and greatly overhaul the current UX/UI to make the new features usable. The overarching plan is to publish an early alpha version in December to allow anyone interested to test the virus gameplay and get an impression of the state of the game. After that I'll proceed with designing either bacteria or the immune system gameplay.

[comments on reddit](https://www.reddit.com/r/roguelikedev/comments/jtqxw2/sharing_saturday_337/)
