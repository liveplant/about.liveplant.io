---
layout: post
title:  "Scratching The Surface"
date:   2015-05-13 19:00:00
categories: meeting
author: Ridwan Hoq
---

##General
###Actions
An action is something that can happen to a plant. For example, watering the plant is an action.

####TBD
- What are potential actions?

###Decision
A decision is a potential action that users can vote on. The decision question should be a yes or no question (yee or nah). There will be a specfied interval for each decision
where user can vote. At the end of that interval, the action (or inaction) will be executed and a new decision will begin.

####TBD
- How long should the decision interval be? (This might be dependent on the various actions)

###Users
User functionality should be as simple as possible while still maintaining some level of identity. Users can only vote once per poll. A user will not have a voting history.

####TBD
- Should users be anonymous?

##liveplant-server
The server is responsible for maintaining the state of the decision. Users and decisions will be stored in a Postgres data store, while the up-to-date vote count on the current 
decision will be stored in Redis. Additionally, the server is responsible for letting the Arduino know what the next action is.

##liveplant-client
The client will visualize a tug of war for the ongoing decision. At its simplest, it could be a bar graph. The client will also display information that informs the decison.

##liveplant-robot
The robot polls the server every 10 seconds for its next action. If the action on the server has a newer timestamp than the last timestamp, then it will execute the action.

###Hardware features
- Internet access
- Water pump
- Indicator light (waiting for action/executing action)
