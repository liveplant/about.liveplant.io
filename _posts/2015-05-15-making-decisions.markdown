---
layout: post
title:  "Meetup Notes: Making Decisions"
date:   2015-05-15 19:00:00
categories: meetup progress
author: Austin Pray
---

[Meetup link for posterity](http://www.meetup.com/Dallas-Web-Mobile-Development-Meetup/events/222218043/).

We made great progress this meetup! We ended up:

- Making a bunch of decisions about the project
- Dividing into [teams](https://github.com/orgs/liveplant/teams)

## Teams

We organized everyone into teams on our GitHub organization. View team
membership over here: [teams](https://github.com/orgs/liveplant/teams).

If you do not see yourself in a team please [email
me](mailto:austin@austinpray.com) and I will get you fixed right up.

### GitHub Team

Everyone be sure to [publicize your liveplant organization membership](https://help.github.com/articles/publicizing-or-hiding-organization-membership/)
over
[here](https://github.com/orgs/liveplant/people).

![instructions](https://i.imgur.com/0o1sPGe.png)

### Team Page

Everyone should also add themselves to [the liveplant team
page](http://about.liveplant.io/team/)! Add your information
[here](https://github.com/liveplant/about.liveplant.io/blob/gh-pages/_data/team.yml).
If you do not know how to add your information I suppose this would be a great
opportunity to learn how to contribute to a project on GitHub. We can go over
this next time we meet. If you want to do a bit of reading on your own visit:
[GitHub help](https://help.github.com/).

## What We Decided

### Defined Robot Actions

So water is definitely going to be what we are starting with as our goal. We
should focus first and foremost on getting this robot to water a plant. All
other enhancements are secondary and pushed until later. However, we thought of
some really cool ideas for later:

- Temperature control
- Grow light
- Play music and have users be able to change music (perhaps public domain music?)
- [Ilumi light](http://ilumi.co/) that users can change the color of.

### Action Frequency

We agreed that the decision making process should be very short lived. The vote
period should last perhaps less than a minute. A user should be able to jump in
and start immediately seeing the fruits of his actions. As such: the actions
will be executed in small increments. For instance: rather than water being
dispensed in large streams it should be dispensed in small squirts.

## Get to Work

### Everyone

- If you want to give legs to your suggestion or discuss something: [make an
  issue](https://help.github.com/articles/creating-an-issue/) on the [relevant
  repo](https://github.com/liveplant).
- Take a look at the existing issues and be sure to give your thoughts.
- As per above: add yourself to the about.liveplant.io team page.

### [Static Website Team](https://github.com/liveplant/about.liveplant.io)

You guys are good to start hacking.

- Homepage needs to be converted into an attractive landing page
- Pages should be created as needed
- The site needs styles 
  - Make decisions on what framework (if any) to use for styles
  - Make issues to discuss design process

### [Robot Team](https://github.com/liveplant/liveplant-bot)

[You guys need to agree on which platform you are going to use](https://github.com/liveplant/liveplant-bot/issues/1).

### [API Server Team](https://github.com/liveplant/liveplant-server)

- [decide hosting](https://github.com/liveplant/liveplant-server/issues/4). Spoiler alert: let's use Heroku lol.
- [start fresh](https://github.com/liveplant/liveplant-server/issues/5)

### [Client Team](https://github.com/liveplant/liveplant.io)

- [decide on which framework](https://github.com/liveplant/liveplant.io/issues/1)
- make issues to discuss and wireframe the actual interface
