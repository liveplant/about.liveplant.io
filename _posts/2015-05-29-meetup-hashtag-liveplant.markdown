---
layout: post
title:  "Meetup Notes: Hashtag Liveplant"
date:   2015-05-29 19:00:00
categories: meetup progress
author: Austin Pray
---

[Meetup link for posterity](http://www.meetup.com/Dallas-Web-Mobile-Development-Meetup/events/222592385/)

## Server

We need to get a [Vagrant][] box up and running so everyone can work on the Server. There is an issue for this task over at [#10](https://github.com/liveplant/liveplant-server/issues/10)

## Client

### UI Components

![diagram](https://i.imgur.com/1TyrrQQ.jpg)

There are four UI components that need to be implemented.

- Actions Panel [discussion](https://github.com/liveplant/liveplant.io/issues/5)
- Stats Box [discussion](https://github.com/liveplant/liveplant.io/issues/6)
- Timeline [discussion](https://github.com/liveplant/liveplant.io/issues/7)
- Live Stream [discussion](https://github.com/liveplant/liveplant.io/issues/8)

### Design

@sutariachintan gave some great suggestions for the front-end design. **Discuss his suggestions [here](https://github.com/liveplant/liveplant.io/issues/4).**

>![img_3069](https://i.imgur.com/4h3NdVM.jpg)
>
>### Top Panel
>- Since video in this project isn't going to be very active (plant doesn't move much), we don't need to make it a huge part of the screen space. In the same panel, we can put three things: 
>     - a graph that shows plant growth over time (could be measured using average number of green pixels captured in a time frame, so that it captures size of plant, health of plant, orientation, etc.)
>     - twitch feed of plant with a scale as the backdrop so there is an easy visual indicator of the height of the plant
>     - basic metrics (days since planting, number of actions voted upon, number of votes cast since start of site, etc.)
>
>### Body
>- Should be structured similar to a Twitter feed in descending order (most current prompt being voted on is on top, oldest prompt is on bottom).
>- The prompt is inside of a rectangular box with a voting icon on either side.
>- Prompts should be phrased in the affirmative and the voting icons on either side should be positive or negative. Example: "Give the plant 1mL of water"
>- Votes will fill the box so that more votes in the left option cause the left side to inch towards the right. Votes towards the right side inch the fill towards the left. This gives it a tug of war effect. There should be a cross over point that once you get a certain number of votes going in a particular direction, it "tilts" and the action is committed.
>
>### Side Bar
>- Chat window
>- Captcha to be populated before sending a chat message
>- Text box with send button


### Implementation

@jhliberty is going to scaffold out the client using [seeds][]. This means we are uing [ember][] as the front-end javascript framework.

## #liveplant

<blockquote class="twitter-tweet" lang="en"><p lang="en" dir="ltr"><a href="https://twitter.com/hashtag/LivePlant?src=hash">#LivePlant</a> video update from <a href="https://twitter.com/nodDFW">@nodDFW</a>! <a href="https://twitter.com/AustinPray">@AustinPray</a> <a href="https://twitter.com/JHLiberty">@JHLiberty</a> <a href="https://twitter.com/TexasCode">@TexasCode</a> <a href="https://twitter.com/bigdcode">@bigdcode</a> <a href="https://twitter.com/tweetmonster999">@tweetmonster999</a> <a href="http://t.co/NMhcS0HcVQ">pic.twitter.com/NMhcS0HcVQ</a></p>&mdash; Chirag Gupta (@ChicagoGupta) <a href="https://twitter.com/ChicagoGupta/status/604475479253393408">May 30, 2015</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" lang="en"><p lang="en" dir="ltr">Beeping lights!! <a href="https://twitter.com/hashtag/liveplant?src=hash">#liveplant</a> <a href="http://t.co/mNUrWK0uQh">pic.twitter.com/mNUrWK0uQh</a></p>&mdash; Austin Pray (@AustinPray) <a href="https://twitter.com/AustinPray/status/604458653396049920">May 30, 2015</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

[seeds]: https://github.com/terminalvelocity/seeds.js
[ember]: http://emberjs.com/
[Vagrant]: https://www.vagrantup.com/
