---
layout: post
title:  Sharing Saturday December 19
description: Sharing Saturday post on r/roguelikedev
---

After the substantial amount of changes over the last month, development is slowing down somewhat. I'm currently testing the virus-related gameplay in combination with the reworked UI.

The idea goes as follows: There are two types of viruses in the game: RNA viruses and retroviruses. Virions (individual virus particles, TIL) will try to attach to nearby cells that have a receptor. In the future this needs to be a matching receptor, but for there is only one generic receptor type for ease of testing.

If an *RNA virus* manages to infect a cell, this cell is forced to replicate the virus and create new virions until its carrying capacity is reached, it bursts and sets them all free to go hunt for more cells.

If a *retrovirus* infects a cell, it's genome (RNA) is transcribed into DNA and inserted into the cell's DNA. From there it can either stay dormant or break out every now and then and force the cell to produce more virions without necessarily dying from it.

The second option has a twofold implication on you, the player. If you're unlucky the virus DNA will add negative traits to your DNA, effectively making you more vulnerable and drain your resources for producing new virions. On the other hand the game will offer the player facilities to modify its DNA, thus allowing to engineer the virus DNA to attack bacteria or cancerous cells instead. That way, being infected can be turned into a substantial benefit.

---

Now I'm looking for an elegant solution for RNA viruses. Currently being infected by those spells inescapable death because there are no ways yet to resist the forced production til the cells bursts. It would be nice to keep these in the game because many viruses operate and harm the body that way. Keep in mind the virus can only attach if the cell has receptors on its surface. Thus trying to keep receptor genes out of your DNA is the best defense against viruses right now. Though even that is always a trade-off because the receptor might also be required for you to interact with other cells. Seems like it could be a lot of work to balance as the danger of viruses and usefulness of the receptor system not only depend on player stats but also on related game content.

I'd be very grateful for any advice on balancing a game with complex inter-dependencies between its subsystems. Cheers!

[comments on reddit](https://www.reddit.com/r/roguelikedev/comments/kfwz2m/sharing_saturday_342/)
