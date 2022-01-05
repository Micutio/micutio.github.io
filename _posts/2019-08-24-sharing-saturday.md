---
layout: post
title:  Sharing Saturday August 24
description: Sharing Saturday post on r/roguelikedev
---

This week good progress was made and the entity generation from DNA has its first working prototype. DNA generation and parsing finally work together and produce usable results. While continuing to clean up the code and hook up the remaining entity attributes to the DNA properties, I've been making plans for the next couple steps. The segmentation of gene traits into the three super traits **sensors**, **processors** and **actuators** seems like a solid idea in hindsight because it allows to elegantly circumvent some potential issues:

First off, representing the DNA to the player. Obviously the best representation of the player DNA is the player object itself since your stats and available actions are determined by your digital genes. However this only tells half the story and I reckon players would actually like to have some colorful bar-code-style visualization of their DNA. I know I would! A three-color bar-code, each gene represented in the color of its super trait, gives us just that: a representation with some information about the nature of our digital genes but without te overwhelming noise of individual gene colors. An even simpler option - possibly for permanent display in the UI - is a little chart with three bars, showing the percentage of sensor, processor and actuator genes in the DNA.

Another issue is generating random dna that still fulfills certain constraints for certain types of entities. For example you might want almost no mobility for wall and floor cells, little mobility and higher aggressiveness for viruses and more mobility for most bacteria. This can be quite easily achieved by defining distributions for each super trait in the entity data files.

To further expand the expressiveness of genome definition I'm also planning on creating a genome library where more complex genes can be composed of the basic attributes and actions that are hard coded in the game.

For example we have the following genes for basic action:
- move
and basic attributes:
- sensor range
- health

From these we can construct more complex genes for flagellum and cilium.
A flagellum is a (sometimes quite sizeable) tail-like appendage that allows for movement but also sensing what's in the immediate vicinity. So a genome for it could look like this:

```txt
+------+--------------+--------+
| move | sensor range | health |
+------+--------------+--------+
```

A cilium (plural: cilia) is a small hair-like extension of the cell which makes them appear all fuzzy and also helps moving them around. Cilia are usually much smaller and more numerous than flagella. They are less useful for sensing, but just as viable motors. A genome from them could look like this:

```txt
+------+------+
| move | move |
+------+------+
```

Creating a library of these higher-level genomes will help generate organisms that can fit certain type categories but are still very much random.

[comments on reddit](https://www.reddit.com/r/roguelikedev/comments/cum45r/sharing_saturday_273/)