---
layout: post
title:  "Meetup Notes: Esoteric JavaScript"
date:   2015-07-10 19:00:00
categories: meetup progress
author: Austin Pray
---

[Meetup link for posterity](http://www.meetup.com/Dallas-Web-Mobile-Development-Meetup/events/223651493/)

## Client

We did some hacking on the front-end this time. We converted our hardcoded templates into React components.

- [VoteCount component](https://github.com/liveplant/liveplant.io/commit/0120d2b341e9f7fe43298a5106b774b95fb1acbd)
- [VoteButtons component](https://github.com/liveplant/liveplant.io/commit/a24efdf2bbccec565c5c945be1ee5ff7894596df)

There is ongoing work you can follow on the [componentize](https://github.com/liveplant/liveplant.io/tree/componentize) branch. 

We need to start giving the application structure and the ability to call the API. I was toying around with [Alt](http://alt.js.org/) but I am open to more options.

Also welcome @georgejdli! He joined the project this week and has been helping with the crazy ES6 side of things.

## Server

@smspence came through with an updated GET `/votes` endpoint. [Check it out](https://github.com/liveplant/liveplant-server/pull/27). We need to hook that endpoint up the UI now.
