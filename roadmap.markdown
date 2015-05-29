---
layout: page
title: Roadmap
permalink: /roadmap/
---

Interested in contributing? Pop over to the [Getting Started][getting-started] page to find how.

## Phase 1: Initial MVP

The first version liveplant will incorporate the following criteria:

- Interface with live feed of plant and ability to submit bot action requests to
  server.
- Server is able to receive requests from liveplant.io interface and submit
  them to bot.
- Bot is able to listen to incoming requests from server.
- Bot is able to water plant.

### Blockers:

#### liveplant.io

- Define action frequency
- Interface needs to be designed.
- [Front-end framework needs to be chosen.](https://github.com/liveplant/liveplant.io/issues/1)

#### liveplant-server

- Go server needs to be bootstrapped.

#### liveplant-bot

- [Microcontroller needs to be decided upon.](https://github.com/liveplant/liveplant-bot/issues/1)

## Phase 2 and beyond:

If you'd like to contribute ideas to what liveplant.io should be able to do
after phase 1 is completed, [submit a ticket][] and prefix the issue title with
"Idea:".

- Temperature control
- Grow light
- Play music and have users be able to change music (perhaps public domain music?)
- [Ilumi light](http://ilumi.co/) that users can change the color of.

[getting-started]: /getting-started/
[submit a ticket]: https://github.com/liveplant/about.liveplant.io/issues/new
