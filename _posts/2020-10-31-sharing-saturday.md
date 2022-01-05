---
layout: post
title:  Sharing Saturday October 31
description: Sharing Saturday post on r/roguelikedev
---

This week saw UI additions for mapping player actions to pre-defined keys and display them in the user interface. Currently player actions distinguish between targeted and non (self)-targeted actions. The arrow keys will trigger the primary action and apply it on the empty tile or object - depending on the action - located in the given direction. The same goes for WASD for triggering the secondary targeted action. The keys 'Q' and 'E' can be bound to primary and secondary self- or un-targeted actions.

Given my limited exposure to traditional rogue-likes I'm not familiar with common control schemes, meaning for now I'll just go with whatever feels right to me.

Now that the core engine including genetics is fleshed out, I'm spending time researching microbiology to come up with a clear plan for the gameplay and most importantly the level of detail with which to implement real-life mechanics. It is supposed to revolve around fighting off viral and bacteria infections inside the host organism, all the while dodging the host's immune system response:

- **The player** is an artificially engineered cell introduced into the host by scientists. This allows for a narrative where the player can make use of various mechanics that in reality are restricted to bacteria, immune response cells and such.

- **Viruses** can infect cells including the player and interrupt their activities to cause them to produce more virus DNA instead and destroying the cell in the process.

- **Bacteria** can directly attack cells and try to multiply their numbers to overpower the defenses. Using plasmids they can propagate part of their DNA and resulting useful and harmful traits. The player will also be able to use plasmids.

- **The immune system** will consist of a number of cells, initially of two: antibodies that directly attack pathogens and memory cells that can trigger quick mass releases of the former. These will attack all objects with certain antigen markers, including the player. One way to avoid getting attacked is to keep distance or manipulate the own genome to drop antigen marker traits.

This ought to be complex enough for now, given the research, implementation, testing and balancing involved.

Also I keep re-reading the old announcement post I did about the game here. You guys had so many good ideas that help me navigate the development. Cheers for that!

[comments on reddit](https://www.reddit.com/r/roguelikedev/comments/jl8q28/sharing_saturday_335/)
