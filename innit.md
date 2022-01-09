---
layout: page
title: Innit
permalink: /innit/
---

## A game about the immune system (alpha 0.0.6)

<canvas id="canvas">
    canvas tag not supported
</canvas>
<script src="/wasm/innit.js"></script>
<script>
    var arrow_keys_handler = function(e) {
        switch(e.code) {
            case "ArrowUp": case "ArrowDown": case "ArrowLeft": case "ArrowRight":
            case "Space": e.preventDefault(); break;
            default: break; // do not block other keys
        }
    };
    window.addEventListener("keydown", arrow_keys_handler, false);
    window.addEventListener("load", async () => {
        await wasm_bindgen("/wasm/innit_bg.wasm");
    });
</script>

<!-- [Play in dedicated tab](https://micutio.github.io/innit.html) -->

## How to play

| Control                                                | Effect                                                  |
| :----------------------------------------------------- | :------------------------------------------------------ |
| Arrow keys                                             | primary action into north, east, south west direction   |
| <kbd>W</kbd>, <kbd>A</kbd>, <kbd>S</kbd>, <kbd>D</kbd> | secondary action into north, east, south west direction |
| <kbd>SHIFT</kbd> + <kbd>P</kbd>                        | reassign primary action                                 |
| <kbd>SHIFT</kbd> + <kbd>S</kbd>                        | reassign secondary action                               |
| <kbd>Q</kbd>                                           | primary quick action on self                            |
| <kbd>SHIFT</kbd> + <kbd>Q</kbd>                        | reassign primary quick action                           |
| <kbd>E</kbd>                                           | secondary quick action on self                          |
| <kbd>SHIFT</kbd> + <kbd>E</kbd>                        | reassign secondary quick action                         |
| <kbd>SPACE</kbd>                                       | pass turn                                               |
| <kbd>C</kbd>                                           | character information                                   |
| <kbd>F1</kbd>                                          | display controls                                        |
| <kbd>1</kbd> - <kbd>8</kbd>                            | change font                                             |
| <kbd>ESC</kbd>                                         | return to main menu controls                            |

## About the game

NOTE: The current alpha version of the game only contains viruses and plasmids. Bacteria are planned but not yet implemented.

The game takes place inside the human body.

It revolves around fighting off viral and bacteria infections inside the host organism, all the while trying not to get caught up in the immune system response yourself.

The player controls an futuristic artificially engineered cell introduced into the host by scientists. You can make use of various mechanics that in reality are restricted to bacteria, immune response cells and such.

### Core mechanics

The core feature of the game is that everything is based on DNA: the player cell, viruses, plasmids and even the tissue that makes up the game world is alive and carries individual DNA. The player can manipulate their own DNA to increase their chances of fighting off the infection. It goes as far as changing you receptors to make yourself immune against viruses and other pathogens.

### NPCs and other objects

Viruses can infect cells including the player and interrupt their activities to cause them to produce more virus DNA instead and destroying the cell in the process.

Plasmids are inanimate objects that can be used to acquire new DNA, manipulate existing one or transfer it to other entities. In the future these will be heavily used by bacteria.
