---
layout: post
title:  Sharing Saturday September 12
description: Sharing Saturday post on r/roguelikedev
---

To my shame it's been almost a year since I last posted. Despite the slow progress I never meant to halt or even abandon development at all and hope to return to at least monthly updates in this subreddit.Part of it is setting smaller, easier attainable goals.

On the flip side now it feels l'm looking at the code with a fresh pair of eyes. It's becoming quite evident which parts of the code are easily readable, documented and have held up well over time and which parts require some refactoring to make it easier to understand in the future. So that's nice at least.

Finally I have a first usable iteration for randomly-generated levels that resemble body cavities. For a while I tried to make use of perlin noise, but I'm finding that cellular automata (CA) are much more intuitive for me personally to "grow" organic-looking levels. The rough algorithm would be first seeding a fully blocking level with a basic shape of open cells and then use the CA rules to carve out more open space from there. This should work well with fractals too, to help generate slightly more complex seeding structures from really simple base shapes. [Here](https://imgur.com/gallery/QfvDSCS) is one example of simple cave (or rather cavity in Innit) generation.

Next on the todo list is getting back into the genetics and trait systems that underlies all entities in the game so I can make a plan for a simple starting set of traits and balancing aspects. As of now sometimes the player's starting cell doesn't have enough genes for actuators - and thus cannot move around. Either the player must be insured to always get actuator genes or, what I would really like, the gameplay would allow for some form of progress without having to move around.

[comments on reddit](https://www.reddit.com/r/roguelikedev/comments/ir28xs/sharing_saturday_328/)
