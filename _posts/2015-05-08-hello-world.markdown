---
layout: post
title:  "Hello World: First Meeting Update"
date:   2015-05-08 19:00:00
categories: progress
author: Austin Pray
---

Today at the [Dallas Web & Mobile Development Meetup][meetup link] we initialized the liveplant.io project! 

## Background

The concept is basically [Twitch Plays Pokémon][] for a taking care of a plant.
A robot is setup to take care of a plant. The robot takes commands from the
internet. A live stream is set up so people can watch the plant grow. The drama
happens when bad internet people try to kill the plant by watering too much,
watering too little, withholding sunlight, etc.

This project goes all the way to [hackdfw][] February 28 - March 1, 2015.
[Darren Cattle][], [Ridwan Hoq][], and I worked for 24 hours straight and were
able to build a rough proof of concept. We did not like how unpolished it was
and the fact that it barely worked. As a result: we put the project aside until
we had more time to build it properly. 

As of today the [Dallas Web & Mobile Development Meetup][meetup link] has
adopted liveplant.io as its social coding project! Yay! Now liveplant.io has
team of people from all sorts of backgrounds to give it a fighting chance at
being awesome!

## liveplant Codebase

All of the code for liveplant is under the [liveplant GitHub organization][liveplant org]. The repos are organized as such:

### [about.liveplant.io][]
This is the code for this website. The purpose of this website it to document
our design decisions. Not only will it help unify the development effort, but
it will explain what liveplant is to the world at large. It is implemented in
jekyll.

### [liveplant-bot][] 
This is the code that runs on the actual hardware that is taking care of the
plant. Right now this is written for Arduino and barely works. I think we are
going to ditch Arduino in favor of a [tessel][].

### [liveplant-server][]
This is the API server that the client will talk to. It will be implemented in [Go][]

### [liveplant.io][]
This is the main attraction. This is the actual web interface that a person
will go to control the robot that takes care of the plant. When you go to
http://liveplant.io it will load this code. The implementation details here
need to be discussed and decided on. If I had my pick: I recommend we implement
this in ES6 with [react][] and [flux][]. ES6 transpilation and ES6 modules will
happen through [babel][] and [browserify][]. As far as the decision to use
flux: I am not totally sure about it. This type of project is what it was built
for specifically but it's definitely a bit strange for people who are used to
traditional MVC. Another option is to use [Ember][] as it might be easier for
newer folks to work on. Angular is not a good fit for this project.

So yeah, react/flux vs Ember. Alternatively we could implement both and see
which one is better!

## Start Hacking

Let's fire up some issues on the project repos and get some design discussion going.

**Some stuff we do have nailed down:**

- We are going to use a Venus fly trap as the plant

**Some immediate action items I can think of:**

- This site needs styling and the homepage needs to be made into a landing page. Start hacking.
- We need to make a decision on what front-end JavaScript framework we are going to use on liveplant.io
- We need to buy a plant
- We need to decide what elements of the plant setup are going to be user controlled (water, temperature, etc.)

## Next Time

[The next meetup is on Friday, May 15, 2015 7:00 PM.][next time] Looking forward to seeing everybody!

[meetup link]: http://www.meetup.com/Dallas-Web-Mobile-Development-Meetup/events/222217421/
[liveplant org]: https://github.com/liveplant
[about.liveplant.io]: https://github.com/liveplant/about.liveplant.io
[liveplant-bot]: https://github.com/liveplant/liveplant-bot
[liveplant-server]: https://github.com/liveplant/liveplant-server
[liveplant.io]: https://github.com/liveplant/liveplant.io
[Darren Cattle]: https://github.com/DarrenCattle
[Ridwan Hoq]: https://github.com/ridhoq
[tessel]: https://tessel.io/
[go]: https://golang.org/
[react]: https://facebook.github.io/react/
[flux]: https://facebook.github.io/flux/
[babel]: https://babeljs.io/
[browserify]: http://browserify.org/
[ember]: http://emberjs.com/
[next time]: http://www.meetup.com/Dallas-Web-Mobile-Development-Meetup/events/222218043/
[hackdfw]: http://hackdfw.com/
[twitch plays pokemon]: https://en.wikipedia.org/wiki/Twitch_Plays_Pok%C3%A9mon
