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
| <kbd>Q</kbd>                                           | primary quick action on self                            |
| <kbd>E</kbd>                                           | secondary quick action on self                          |
| <kbd>space</kbd>                                       | pass turn                                               |
| <kbd>C</kbd>                                           | character information                                   |
