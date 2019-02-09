---
layout: page
title: The CAB Project
permalink: /cab_project/
---

### The Concept of the CAB Project

This blog is part of the __Complex Automaton Base__ (CAB) project. The CAB is a base or framework for computer
simulations. These take place in a discretized space, the so called
[cellular automaton](https://en.wikipedia.org/wiki/Cellular_automaton) which at its core is a grid of cells, each
carrying its own internal state. A state change in a cell is often dependent on the states of its neighboring cells.
This makes cellular automata an ideal tool to model and simulate spatial propagation properties, like the spread of
forest fires, percolation through different layers of soil and heat convection.

---

One of the most popular implementations of the CA is the
[Game of Life](https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life) by John Conway. In this model cells have two
states: they can be either dead or alive. Which state they are is given by a set of rules.

* If the cell is alive and has fewer than two live neighbors, it dies, as in underpopulation.
* If the cell is alive and has two or three live neighbors, it stays alive.
* If the cell is alive and has more than three live neighbors, it dies, as in overpopulation.
* If the cell is dead and has three live neighbors, it comes alive, as in reproduction.

At the start of the game, all cells are randomly set to being alive or dead. Then the automaton repeats its update
cycle.

---

Additionally the CAB also allows to
create an [agent-based systems](https://en.wikipedia.org/wiki/Agent-based_model) on top of the cellular automaton.
Agents are autonomously 'thinking' entities which can act and interact with each other. Agent-based systems are often
used to model and simulate interactions and behavior between people, robots - or on more abstract levels computers in
networks.

By combining both approaches - which is commonly referred to as _Complex Automaton_ - the CAB allows agents to act and
interact within a two-dimensional space. Using the cell states and update functions allows agents to manipulate not
only themselves but also the space they are living in.

### Inspiration for the CAB

A couple years back during research work I came across the [MASON](https://cs.gmu.edu/~eclab/projects/mason/)
simulation framework and used it for some of my own experiments. MASON is a very powerful tool that helps build a wide
range of simulations and comes with a lot examples that are thoroughly interesting to play with. When using it for
quickly prototyping simulations however it felt somewhat clunky at times. The sheer number of Java interfaces and
generic programming that makes MASON so powerful also make it hard to understand its inner workings and get going with
new experiments from scratch.

Coincidentally at the same time I started learning [Python](https://www.python.org/) and figured that it makes for a
number of good programming exercises to reimagine a MASON-like framework in Python. The main design goal of this
project is to make creating agent-based and/or cellular simulations as quick and easy as possible. This way more time
can be spent on designing and prototyping simulations and less time on implementing work.

<!-- ### Create your own experiments
TODO: Create new graphic and write tutorial on how to create custom simulations
TODO: Add more images in general here.
![CAB Organization]({{base}}/img/cab_organization_1.png "CAB architecture overview") -->
