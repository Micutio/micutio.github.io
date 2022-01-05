---
layout: post
title:  Sharing Saturday March 27
description: Sharing Saturday post on r/roguelikedev
---

After getting proper tooltips done I moved on to implementing the genome editor. This is an in-game tool available to the player if they have any plasmids inside their cell (inventory).
The editor allows to manipulate the player genes to adapt to their environment. Currently it's supposed to support moving genes between alleles, removing genes, copying genes and inserting new ones. Also planned is intentional random mutation a.k.a. flipping a bit in the binary representation in the genome.

Now, gameplay-wise, initially I planned to apply the genome changes to the player immediately. But in nature this happens over time as the body regenerates or reproduces and the genome is read to (re)build the body. So I reckon it makes more sense to just store the changed DNA and use it once the player cell reproduces an offspring via mitosis. The player would have to regularly 'reincarnate' so to speak to counteract and reset the aging process of the cell.

By this delayed activation of manipulated genes the player has more room to plan and is not necessarily doomed immediately if an unforeseen mutation or manipulation happens.

Ideally I'd have a working version of the gene manipulator by the end of next week. Then I'd have a look at the reproduction mechanic.

[comments on reddit](https://www.reddit.com/r/roguelikedev/comments/me1lyf/sharing_saturday_355/)
