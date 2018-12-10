---
layout: page
title: The CAB Project
permalink: /cab_project/
---


## The Complex Automaton Base Project

The [CAB](https://github.com/Micutio/ComplexAutomatonBase) is a lightweight
framework that is designed to create customized complex automata rapidly and
with ease. Complex Automata are composed of cellular automata (CA) and
agent-based models (ABM).


## Cellular Automaton

A [cellular automaton](https://en.wikipedia.org/wiki/Cellular_automaton) essentially is a regular grid of cells. Each
of its cells can 'look' at its neighboring cells and update its own properties depending on the neighbor states. A
typical CA update cycle has all the cells within the automaton carry out their update methods.

CAs are a great model to explore the propagation of states or attributes through space because of the cell's dependency
on their spatial neighborhood. Some popular applications for CA models are spread of forest fires, floods and similar
spatially focused scenarios.

### Example: The Game of Life

One of the most popular implementations of the CA is the
[Game of Life](https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life) by John Conway. In this model cells have two
states: they can be either dead or alive. Which state they are is given by a set of rules.

* If the cell is alive and has fewer than two live neighbors, it dies, as in underpopulation.
* If the cell is alive and has two or three live neighbors, it stays alive.
* If the cell is alive and has more than three live neighbors, it dies, as in overpopulation.
* If the cell is dead and has three live neighbors, it comes alive, as in reproduction.

At the start of the game, all cells are randomly set to being alive or dead. Then the automaton repeats its update
cycle.

## Agent-based Model

Under construction

# Create your own agents & cells and plug them into the system

![CAB Organization]({{base}}/img/cab_organization_1.png "CAB architecture overview")