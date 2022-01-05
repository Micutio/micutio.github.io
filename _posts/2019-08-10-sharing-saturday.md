---
layout: post
title:  Sharing Saturday August 10
description: Sharing Saturday post on r/roguelikedev
---

## Innit

This week another step towards DNA generation was taken by implementing a seedable, serializable random number generator. Now the RNG can be kept consistent and repeatable even throughout saving and restoring the game state. Keeping the RNG generic allows to switch out the underlying implementation. There are many different RNGs with their own strengths and weaknesses and some are probably better suited for game development than others. I'll leave the research on that to future me.

What's more important right now is repeatability, to help test heavily RNG-dependant features like generating DNA and worlds/dungeons.

As for the overarching task of generating and decoding DNA, I've hit a bit of a speedbump. On one hand DNA generation was pretty easy, as in: randomly take a trait from the list and append the following fields to the DNA

```txt
+------+----------+-----------------------+--------+    +--------+
| 0x00 | trait id | length attribute list | attr 1 | .. | attr N |
+------+----------+-----------------------+--------+    +--------+
```

On the other hand, decoding the DNA back to traits and performable actions
is a little less straight forward. The way I sketched out the decoding feels pretty messy right now and would make adding new traits a bit of a hassle.

For example, some attributes of the trait - or of the action an individual gains through a trait - are determined by how often the gene with this trait id occurs in the DNA string. Furthermore, all traits belong to one of three "super traits": sensing, processing and actuating through which they should be accessed and managed. Eventually the actions then have to get key bindings to let the player use them.

Following the wise old rule of "when in doubt, add another layer of abstraction" my current plan involves to create a gene "library" that deals with most of the aforementioned issues. Genes will be read from a data file and the library would handle all the mappings to actions, super traits and such.
An important requirement for this was the realization that there will be more genes than actions, or to put it in other words: I can predefine a bunch of actions and just associate a trait with one of those. There is no need to code individual actions for each gene. Take for example flagella and cilia, both flexible extensions of cells. They look different, work somewhat differently but serve the same purpose: moving the cell around. Instead of implementing a separate flagellate movement and ciliate movement I can rather implement a general move action and parameterize it with attributes from either gene.

The actions that I have defined so far:

* Sensing
  * sense
* Processing
  * set quick action (a.k.a reflex)
  * set primary/secondary action
* Actuating
  * move
  * attack
  * defend
  * rest

should allow the definition of a pretty decent variety of genes.

[comments on reddit](https://www.reddit.com/r/roguelikedev/comments/cobk2q/sharing_saturday_271/)