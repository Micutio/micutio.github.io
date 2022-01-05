---
layout: post
title:  Sharing Saturday July 24
description: Sharing Saturday post on r/roguelikedev
---

Despite the lack of updates over the past couple weeks this project is still very much alive and well. Part of the reason why progress has slowed a bit this time around is that the feature(s) requires a couple systems to interact with each other.

**Organic Growth / Reproduction**

The major goal of current development is to enable cells that make up the world to die and reproduce, just like our own skin and tissue. Rather than generating a world of fixed wall and floor tiles, the world gen will be distributing "growth chemicals" across the map in varying concentration and set up initial wall cells. Once the wall cells hit their regular end of life they may create offspring and die. The decision on where to place new tissue cells is based on the concentration of the growth chemical. So ideally the world will stay roughly the same shape but allows for slightly changing wall over time. This should drastically improve the feeling of being inside a living organism.

To realise this, several aspects need to be implemented into the game:

1. The cell kill switch, mostly know as programmed cell suicide. This prevents cells from living longer than they're supposed to be and becoming cancerous.

This is currently done in a very simplified way, using a simple counter that will enable the suicide action for the given cell after it has lived for a given number of turns.

2. The improved cellular automaton based world generator

I've decided to create a separate cellular automaton library in Rust to help ease setting up world generators with different rules and cell types. Also I want to have a standalone library for other CA experiments in Rust. The repository can be found [here](https://github.com/Micutio/casim). It's still in the draft/early development phase, but is should soon be decently featured enough to be used for world generation in Innit.

3. Cell reproduction, e.g. binary fission

This one is on hold until I'm done with (2).

In other News I updated the [UI history screenshot album](https://imgur.com/a/jzRDMaq) with a new entry to show off the reworked color scheme and slightly tweaked UI elements. We've got particles now, baby!

[comments on reddit](https://www.reddit.com/r/roguelikedev/comments/oqesef/sharing_saturday_372/)
