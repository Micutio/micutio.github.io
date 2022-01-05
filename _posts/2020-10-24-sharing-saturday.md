---
layout: post
title:  Sharing Saturday October 24
description: Sharing Saturday post on r/roguelikedev
---

The engine reworks from earlier this month are beginning to pay off, because this week has been productive:

- An energy system was introduced by adding genetic traits for energy storage as well as recovery rate. Energy costs for actions had been in place before and now can finally be used.

- The second addition is random mutations of the DNA. Objects now have a parameter indicating the chance of mutation per turn, which will be especially frequent for viruses. Since the DNA uses Gray Code to encode traits, flipping a single bit should have an increased likelyhood of turning one trait into another from the same trait family or at least a valid trait at all. However, because of the small amount of implemented traits so far (6 out of 265) and possible overlap of genes, mutating often turns one trait into one or two pieces of "junk DNA". This makes mutation rather dangerous right now, as it can mean the loss of actions or decrease of character stats. It'll be a lot of fun to explore and balance this mechanic, I reckon.

- The third new feature also relates to the DNA, specifically how to display it to the user. [Here is a quick comparison screenshot between the old and new UI.](https://imgur.com/a/jzRDMaq) A new sidebar was addedn to the right side to show the complete DNA. Previously the DNA was shown in two bars in the bottom panel: one with all non-junk traits and a second one with the same traits but grouped by trait families (actuating, processing, sensing). I found those were not nice to look at and would quickly run out of space with longer DNA.

- A few color tweaks to the UI for consistency and the 'terrain' to blend icons and color better for walkable terrain.

The next week(s) will involve the management of the actions the player gains from their DNA, mainly key bindings for primary, secondary and untargeted actions as well as their assignment from the pool of actions available to the player.

[comments on reddit](https://www.reddit.com/r/roguelikedev/comments/jgxgoi/sharing_saturday_334/)