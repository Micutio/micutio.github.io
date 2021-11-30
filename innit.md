---
layout: page
title: Innit - An immune system roguelike
permalink: /innit/
---

## Innit (alpha 0.0.4)

<canvas id="canvas" height="450" width="750">
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

The game is set to take place inside a living organism that is not specified further but will resemble humans, given that most game-play mechanics are derived from actual biological processes in humans and/or animals.

It is supposed to revolve around fighting off viral and bacteria infections inside the host organism, all the while trying not to get caught up in the host's immune system response yourself.

The player is an artificially engineered cell introduced into the host by scientists. This allows for a narrative where the player can make use of various mechanics that in reality are restricted to bacteria, immune response cells and such.

### NPCs and other objects

Viruses can infect cells including the player and interrupt their activities to cause them to produce more virus DNA instead and destroying the cell in the process.

Bacteria can directly attack cells and try to multiply their numbers to overpower the defenses. Using plasmids they can propagate part of their DNA and the resulting useful and harmful traits. The player is also able to use plasmids.

The immune system will consist of a number of cells, initially of two: antibodies that directly attack pathogens and memory cells that can trigger quick mass releases of the former. These will attack all objects with certain antigen markers, including the player. One way to avoid getting attacked is to keep distance or manipulate the own genome to drop antigen marker traits.
