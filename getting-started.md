---
layout: page
title: Getting Started
permalink: /getting-started/
---

Welcome to liveplant! Here's what you need to know to get started:

### What is liveplant.io?

liveplant.io is a project that was originally started by [Austin][austin],
[Darren][darren], and [Rid][rid] at a [hackdfw][] project a while back. It was
presented at the [Dallas Web & Mobile Development Meetup][meetup-link] as a way for
people of all experience levels to learn more about development. You can learn
more about it's history [here][liveplant-history].

It's divided up into four sub-projects:

- [about.liveplant.io][]: The site you're looking at now!
  Jekyll site for documenting decisions and progress of the project.
- [liveplant.io][]: The front-end. This will be a single-page app that
  has a livefeed of the plant and actions to care for the plant.
- [liveplant-server][]: The API server the client will talk to. It will be implemented in [Go][]
- [liveplant-bot][]: An (insert tbd microcontroller here) project that
  will power the bot caring for the plant and reporting statistics such
  as humidity, temperature, etc.

### Phase 1: Initial MVP

The first version liveplant will incorporate the following criteria:

- Interface with livefeed of plant and ability to submit bot action requests to
  server.
- Server is able to receive requests from liveplant.io interface and submit
  them to bot.
- Bot is able to listen to incoming requests from server.
- Bot is able to water plant.

#### Current blockers:

- liveplant.io: Interface needs to be designed.
- liveplant.io: Front-end framework needs to be chosen.
- liveplant-server: Go server needs to be bootstrapped.
- liveplant-bot: Microcontroller needs to be decided upon.

### Phase 2 and beyond:

If you'd like to contribute ideas to what liveplant.io should be able to do
after phase 1 is completed, [submit a ticket][] and prefix the issue title with
"Idea:".

### How can I help?

Come to the meetups and contribute!

- Want to sling some html+css? Join the [about.liveplant.io][] team.
- Have you been wanting to learn how to write a single page app? Join the [liveplant.io][] team.
- Interested in learning [Go][]? Join the [liveplant-server][] team.
- Want to hack on some hardware? Join the [liveplant-bot][] team.

We look forward to seeing you at [the meetups][meetup-link]!

### Any plans to monetize?

Not at the moment. The goal of the project is to be educational.


[austin]: https://github.com/austinpray
[darren]: https://github.com/darrencattle
[rid]: https://github.com/ridhoq
[meetup-link]: http://www.meetup.com/Dallas-Web-Mobile-Development-Meetup/
[liveplant-history]: /meetup/progress/2015/05/08/hello-world.html
[about.liveplant.io]: https://github.com/liveplant/about.liveplant.io
[liveplant.io]: https://github.com/liveplant/liveplant-server
[liveplant-server]: https://github.com/liveplant/liveplant-bot
[liveplant-bot]: https://github.com/liveplant/liveplant.io
[go]: https://golang.org/
[hackdfw]: http://hackdfw.com/
[submit a ticket]: https://github.com/liveplant/about.liveplant.io/issues/new
