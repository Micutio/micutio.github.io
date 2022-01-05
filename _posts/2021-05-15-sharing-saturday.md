---
layout: post
title:  Sharing Saturday May 15
description: Sharing Saturday post on r/roguelikedev
---

Progress over the last month has been slow but steady, as is par for the course for a hobby project that you only get to work on after hours. Accordingly I have shifted to updating monthly rather than weekly because there is just more to tell and it evens out the variance between weeks where nothing happens and weeks with notable progress.

For quite a while development has been towards a playable alpha version that is intended to be publicly available for testing and frankly I am scared that people will think it either too boring or too complicated to further engage with it. This fear is nurtured by having seemingly little to show for a significant investment of time and effort into the development.

The past four weeks have had the overarching theme of _grounding_ the development. In short this meant less time spent working on flashy features or engine refinement and more on the tedious work of polishing and bug hunting.

One of the best examples of this is the genome manipulator. For context, the intended use is to choose a gene from your DNA and a function to perform, like mutating, duplicating and removing. So far so easy, but if I'm honest with myself for being a core part of the game mechanic, it is way too unintuitive to use. The coloring of the UI elements is all over the place and there is no hint about how to use it. This one has seen a bunch of polish updates which has shown me how difficult a simple and easy to use UI can be.

Other changes in list form:

**Features**

- inventory system including pick-up and drop item actions
- plasmids, the in-game vehicle for the genome editor
- info screen with controls, accessible via <kbd>F1</kbd>

**Engine**

- particle system
- refactor game environment variables, color palette and particle system to be global singletons (lazy_static)

**Fixes**

- world render bleeding through main menu background image
- sneaky iter().flatten().position() bug leading to picking up random objects into inventory
- limiting spammy consecutive messages to only one at a time in the log
- several crashes and missing ui-updates
- being able to use actions with energy cost higher that max available

[comments on reddit](https://www.reddit.com/r/roguelikedev/comments/nck6ur/sharing_saturday_362/)
