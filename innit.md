---
layout: page
title: Innit
permalink: /innit/
---

<p>
    <canvas id="canvas" height="450" width="750">
        canvas tag not supported
    </canvas>
    <script src="/wasm/innit.js"></script>
    <script>
        window.addEventListener("load", async () => {
            await wasm_bindgen("/wasm/innit_bg.wasm");
        });
    </script>
</p>
