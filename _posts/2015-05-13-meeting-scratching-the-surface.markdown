---
layout: post
title:  "Meeting Notes: Scratching The Surface"
date:   2015-05-13 19:00:00
categories: meeting
author: Ridwan Hoq
---

Meeting between Ridwan Hoq and Austin Pray. The goals of this meeting:

- Unpack and enumerate the basic functionality
- Basic implementation details
- Discuss what problems need to be solved

## Project-wide Concepts

### Actions
An action is something that can happen to a plant. For example, watering the plant is an action.

#### TBD

- What are potential actions?

### Decision

A decision is a vote to determine what the next action is going to be. There will be a specified interval for each decision
where user can vote. At the end of that interval, the action (or inaction) will be executed and a new decision will begin.

#### TBD

- How long should the decision interval be? (This might be dependent on the various actions)

### Users
User functionality should be as simple as possible while still maintaining some level of identity. Users can only vote once per poll. A user will not have a voting history.

#### TBD

- Should users be anonymous?
- How can we discourage bots (captchas, etc.)?

## liveplant-server
The server is responsible for maintaining the state of the decision. Users and decisions will be stored in a Postgres database, while the up-to-date vote count on the current 
decision will be stored in Redis. Additionally, the server is responsible for letting the Arduino know what the next action is.

## liveplant-client
The client will visualize a tug of war for the ongoing decision. At its simplest, it could be a bar graph. The client will also display information that informs the decision.

## liveplant-robot
The robot polls the server every 10 seconds for its next action. If the action on the server has a newer timestamps than the last time stamp, then it will execute the action.

### Hardware features
- Internet access
- Water pump
- Indicator light (waiting for action/executing action)
