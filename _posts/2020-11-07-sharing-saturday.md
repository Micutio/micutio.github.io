---
layout: post
title:  Sharing Saturday November 07
description: Sharing Saturday post on r/roguelikedev
---

This week was very diverse in workload. First off, code refactoring and clean up from the previous week. So far the AI system was still strongly based on the tutorial with which I started the game: the game entities have an optional `AI` component that would be used for determining the next action, if present. If not present, the entity would be controlled by the player. With the new version, the former `AI` component is now a `Controller` component that can be either `Npc`, `Player` or `Inactive`. This allows to take all the player control logic out of the entity struct, slimming it down a fair bit. As a additional bonus, this simplifies handling control changes in the event that a player may take over an npc-controlled cell or vice versa.

Then I started implementing the gameplay mechanics laid out in last Saturday's post:

1. an inventory for storing any entities that might reside inside a cell, e.g.: viruses or plasmids
2. plasmid DNA - if objects carrying this enter another objects inventory, this will then be considered part of the player's DNA

Furthermore I went and did research on RNA-viruses and retroviruses to get a better idea of how to implement the next bits of gameplay.

In summary adding the content and extending the game engine this week went without a hitch and satisfyingly elegant, which validates the recent sweeping refactoring and improvements to the engine architecture.

Next week will be all about viruses with a bit more research and hopefully complete first revision of the virus gameplay.

[comments on reddit](https://www.reddit.com/r/roguelikedev/comments/jpgiog/sharing_saturday_336/)