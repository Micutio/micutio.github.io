---
layout: page
title: The CAB Project
permalink: /cab_project/
---

## The Concept of the CAB Project

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

## Implementation and Programming of the CAB

The CAB is written in the [Python](https://www.python.org/) programming language and designed to make creating agent-
based and/or cellular simulations as quick and easy as possible. This way more time can be spent on designing and
prototyping models & simulations and less time on implementing them.

## Create your own experiments

![CAB Organization]({{base}}/img/cab_organization_1.png "CAB architecture overview")
