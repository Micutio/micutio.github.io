---
layout: post
title:  Initial announcement on reddit
description: Initial announcement of Innit on r/roguelikedev
---

In 2018 I joined the [r/roguelikedev](https://www.reddit.com/r/roguelikedev/) subreddit and started doing the libtcod tutorial for Rust, on how to program a roguelike.
While following along I started to develop the initial idea for **Innit**.
The following post was the first published description of it.

<br>

---

<br>


Greetings! This shall be the inaugural post for my project "Innit".

## Backstory

A while ago I discovered this forum and the Rust libtcod tutorial. Since this seemed a good way to get more development experience in Rust under my belt I followed along and eventually got hooked. Previously I had only played a couple of roguelites, including Dwarf Fortress, Diablo and Torchlight, but never really dug deeper into the proper genre. So that's my prior experience: lacking, to say the least.

Nevertheless, while wrapping up the tutorial I drafted an outline to continue the project. For reasons you will learn throughout the rest of this post, the game needs to be able to treat everything as an actor, even the tiles that make up the game world. That meant, before starting to implement any kind of content, a huge chunk of time was spent on refactoring the bare-bones tutorial engine into a ["Hauberk"-style](https://journal.stuffwithstuff.com/2014/07/15/a-turn-based-game-loop/) game loop and I/O handling.

This process is still in the finishing stages, hence there exists only a very minimal prototype of the game right now. And despite being very time-consuming, it did prompt me to think a lot about game design, Rust programming patterns and all kinds of things.

> Note to self: I should really start getting into the habit of writing blog posts about my projects.

## Setting: A living breathing World

You, the player, are controlling a microbe life form. The world you're living and moving in is a larger sentient organism. It's not clear yet as to whether this organism is of human, animal or alien nature, or something else entirely. The point is, it's a living and breathing world. All around you are body cells of the host, bacteria, viruses and other microbial life. Your goal in the game is not quite determined yet, but it will revolve around helping your host to fight off diseases and prevent it from dying. After all, if your host dies, so do you! Use the host's capabilities like immune system memory, antibodies and fevers to help get rid of unwanted intruders, but be careful not to get caught in the crossfire. Immune systems are know to overreact at times or attack benign cells without hesitation.

> I am drawing lots of inspiration here from the Kurzgesagt [Medicine and Biology playlist](https://youtu.be/YI3tsmFsrOg) on Youtube, especially the [Microbiome](https://youtu.be/VzPD009qTN4). Another motivation for the general setting comes straight out of my childhood, a brilliant series named [Once Upon a Time... Life](https://en.wikipedia.org/wiki/Once_Upon_a_Time..._Life).

To me microbiology seems like a good setting for an ASCII roguelike, because it is quite abstract to most people (myself included). Characters and symbols are a decent approximation of many of these lifeforms. In addition organic worlds also allow for very eye-catching color schemes (bright pink anyone?), bringing a little more uniqueness to the game.

## The Game Hook: Player DNA

The player's microbe character is based on a strand of DNA. All attributes and skills are supposed to be encoded in it. Over the course of the game the character can extend, reduce and mutate its own DNA to change said skills and attributes.

DNA will most likely be acquired from other life forms via combat but this is open for debate. DNA should be able to be represented as a string of binary or hexadecimal numbers, to make it easy to modify and randomly generate player characters. This could go as far as using the DNA as a score or hall of fame for your character in case you would like to revisit one of your incarnations at a later time again.

## The mechanics behind the DNA

This is really the major challenge of this project; designing a way to encode and decode skills and attributes in a DNA that can be easily mutated, taken apart and stitched together and still be a likely valid expression afterwards.

My best guess so far is to try and break down attributes and skills into three categories:

- sensors - attributes and methods for perceiving the environment e.g, range of sight
- processors - attributes and methods for digesting information, mostly relevant for the AI
- actuators - attributes and methods for manipulating the environment e.g., movement and interaction

and separate attributes and methods into these categories. The AI could then go through this whole process of _sensing the environment -> processing available information -> take action_, either in form of randomly selecting available methods or traversing a decision tree.

You can find more ideas on this, beyond the scope of this introductory post, in the Projects and Wiki sections on GitHub (link at the bottom of this post). I'll try to keep them updated as I continue development.

All entities in the game; player, NPCs and even the world tiles are planned to be generated from and contain their own dna. This could allow for mechanics like cancer where wall tiles can start to replicate out of control, threatening to narrow down or even close passages.

## Outlook

I'm trying not to bite off more than I can chew for a first-time game development project. Next order of business will be to just get a minimal version of character generation from DNA working, or at least a stable API thereof. Once that's accomplished we'll have the mold that the rest of the game's content can fit into.

Ultimately though there are so many concepts Innit can borrow from biology and chemistry that I could keep this going as long as it's fun and as long as I'm willing to put in the research.

> **Disclaimer:** I am not educated in any natural science and while I try to keep the setting and core mechanics "based on" real biology, don't ever take my word for it :-)

Thank you for bearing with me through this wall of text. I more than welcome any discussion and suggestions and will try my best to keep you posted with regular updates on Sharing Saturdays.


[view on reddit](https://www.reddit.com/r/roguelikedev/comments/cf62b5/introducing_innit_your_100_organic_roguelike/)