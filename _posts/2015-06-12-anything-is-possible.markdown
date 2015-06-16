---
layout: post
title:  "Meetup Notes: Anything is Possible"
date:   2015-06-12 19:00:00
categories: meetup progress
author: Austin Pray
---

[Meetup link for posterity.](http://www.meetup.com/Dallas-Web-Mobile-Development-Meetup/events/223056727/)

# Robot

## New Member: Zach Stokes

Zach Stokes (@DeftxPunk) has joined the project! Why is this so exciting? He
has direct experience putting together an IoT hydroponics robot!

[Check out the kickstarter page for "The Root".](https://www.kickstarter.com/projects/57013250/the-root-a-self-contained-solar-powered-plant-grow)

We look forward to see him dropping some knowledge on us and getting the ball
rolling over on [the robot repo](https://github.com/liveplant/liveplant-bot).

# Server Stuff

## Housekeeping

Took care of some housekeeping on [liveplant server](https://github.com/liveplant/liveplant-server).

- [Added cors](https://github.com/liveplant/liveplant-server/issues/14)
- [Added support for OPTIONS](https://github.com/liveplant/liveplant-server/issues/14)

## 1.0.0 milestone

I went ahead and set up a milestone for issues that are direct action items: [1.0.0 milestone](https://github.com/liveplant/liveplant-server/milestones/1.0.0).

Issues that have been added to this 1.0.0 milestone can be considered ready to
be implemented and are blocking the project completion. Feel free to claim an
issue and make it your own.

## Building and Running liveplant-server on Windows

I was able to build and run liveplant-server on Windows using [Cygwin](https://www.cygwin.com/).
If you are a Windows user and want to contribute to server development, I
recommend [installing Cygwin](https://cygwin.com/install.html), and making sure
the OpenSSH package is installed. Packages can be added and installed at any time using
the Cygwin installer. The OpenSSH package I am using can be found using the Cygwin installer
under the name / description "openssh: The OpenSSH server and client programs
(installed binaries and support files)". For posterity, the exact package I installed
is named `openssh-6.8p1-1`.

Launch your Cygwin terminal and `cd` to your `liveplant-server` directory.
From there, since we are currently using [Vagrant](https://www.vagrantup.com/)
for running our development environment, just run `vagrant up` and then `vagrant ssh`
to get into the Vagrant virtual machine. From there, you can run `make` to build and
then `liveplant-server` to begin running the server.

# Client

Nothing notable to report. Check the [existing open issues](https://github.com/liveplant/liveplant.io/issues).

Discussion about the strategy going forward is happening
[here](https://github.com/liveplant/liveplant.io/issues/10) and
[here](https://github.com/liveplant/liveplant.io/issues/1). Input is needed.
