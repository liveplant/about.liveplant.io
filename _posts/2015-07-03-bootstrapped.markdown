---
layout: post
title:  "Meetup Notes: Bootstrapped"
date:   2015-07-03 19:00:00
categories: meetup progress
author: Austin Pray
---

[Meetup link][] for posterity.

Today we started implementing the front-end. Here is how far we got:

![liveplant screenshot](https://i.imgur.com/2QVeGzj.png)

Our goal was to start from scratch and get to the point where clicking buttons
in the "Vote" section would manipulate the numbers in the "Current Vote"
section and the "Current Action". We didn't quite get there but we made a lot
of good progress.

## Front-end Progress

You can see all the changes we made at the meetup today at [this][meetup
progress] commit. Here is the [pull request][] for the changes.

- [Add a node .gitignore](https://github.com/liveplant/liveplant.io/blob/f28614ebc6189f8642e0b3bbdc487293a41d68d5/.gitignore)
- [Create a Makefile to build the project's source files](https://github.com/liveplant/liveplant.io/blob/f28614ebc6189f8642e0b3bbdc487293a41d68d5/Makefile)
- [Initialize a package.json and add some dependencies](https://github.com/liveplant/liveplant.io/blob/f28614ebc6189f8642e0b3bbdc487293a41d68d5/package.json)
- [Create a base index.html from html 5 boilerplate](https://github.com/liveplant/liveplant.io/blob/f28614ebc6189f8642e0b3bbdc487293a41d68d5/src/index.html)
- [Create a javascript entry point](https://github.com/liveplant/liveplant.io/blob/f28614ebc6189f8642e0b3bbdc487293a41d68d5/src/js/index.js)
- [Create an Action model](https://github.com/liveplant/liveplant.io/blob/f28614ebc6189f8642e0b3bbdc487293a41d68d5/src/js/models/Action.js)

## Front-end Design Decisions

### Bootstrap

For this initial implementation we are using [Bootstrap 3][]. I am pretty sure
we want to use [Semantic UI][] eventually. Right now it simply doesn't matter
and we need to get something on the page as quick as possible. I am slightly
concerned that [Semantic UI][] (and even [Bootstrap][] for that matter) is
overkill for our single view application, but we don't even have to start
thinking about such things yet.

### JavaScript Setup

Take a look at the
[package.json](https://github.com/liveplant/liveplant.io/blob/f28614ebc6189f8642e0b3bbdc487293a41d68d5/package.json)
for a full list of the dependencies.

Development side:

- [browserify][] to give us JavaScript modules.
- [babel(ify)][babel] to give us ES6 transpilation.

Browser Side:

- [backbone][] gives our application some structure. It is not currently being used at all but we might use it. ES6 classes and such might actually make backbone obsolete for our use case.
- [react][] is also not currently being used but I plan for react to be our view layer.
- [jQuery][] for making server requests and stuff. We might not need this but mind as well include it to start. Since we are only targeting modern browsers I can totally see us removing this.
- [lodash][] because I like lodash. I can't imagine writing JavaScript without lodash.

### Project Build Step

We are using [GNU Make][] to orchestrate all the commands that build our source
files into compiled distribution files. A lot of people are familiar with tools
like [Grunt][] and [gulp][] for building JavaScript projects and might wonder
why we are not using one of those. [GNU Make][] is pretty much the pinnacle of
build tools. We would have to install 10 plugins and before we even scratch the
surface of the features Make has out of the box.

Running `make` inside the project directory will build all the source files and
throw the compiled versions into the `dist/` folder. Upload the contents of the
`dist/` folder to a static file hosting service such as AWS S3 and be done with
it.

## Next Steps for Front-end

Break the current hardcoded index.html into React components. Perhaps start
interacting with the server.

## Server Progress

@smspence made some good progress on the server! Before the `current_action`
endpoint was hardcoded to output `water` each time it was called. Now it will
actually compare the collected votes and output which one is greater.

[Check out his pull request](https://github.com/liveplant/liveplant-server/pull/24).

![liveplant whiteboard](https://i.imgur.com/CQr2Fb6.jpg)

[Meetup link]: http://www.meetup.com/Dallas-Web-Mobile-Development-Meetup/events/223546178/
[meetup progress]: https://github.com/liveplant/liveplant.io/commit/f28614ebc6189f8642e0b3bbdc487293a41d68d5
[pull requiest]: https://github.com/liveplant/liveplant.io/pull/14
[Bootstrap 3]: http://getbootstrap.com/
[Bootstrap]: http://getbootstrap.com/
[Semantic UI]: http://www.semantic-ui.com/
[babel]: https://babeljs.io/
[browserify]: http://browserify.org/
[backbone]: http://backbonejs.org/
[react]: https://facebook.github.io/react/
[jQuery]: https://jquery.com/
[lodash]: https://lodash.com/
[GNU Make]: https://www.gnu.org/software/make/
[gulp]: http://gulpjs.com/
[Grunt]: http://gruntjs.com/
