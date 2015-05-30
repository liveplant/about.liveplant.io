---
layout: post
title:  "Server Pair Programming Session 1"
date:   2015-05-28 20:49:00
categories: work pair_programming_session
author: Austin Pray
---

These notes are from a pair programming session between @austinpray and @ridhoq.

@darrencattle @austinpray (me) @ridhoq were in attendance.

## Overview

We tracked our progress over here: [issue #7](https://github.com/liveplant/liveplant-server/issues/7)

At the time of writing this is how far we got:

- **☑︎ Determine what the JSON response looks like. This is what the bot will be consuming.**
- **☑︎ Document API usage in the README**
- **☑︎ Scaffold repo #5**
- Scaffolding includes setting up Redis
- Write failing tests for the response
- Write code to satisfy test
- **☑︎ Ship to heroku #4**

Nothing is actually saving in any databases or anything, it's just returning a
valid JSON response. With the timestamp being the server time and the action
always being to water.


## Next steps

### Refactor

- Break main.go into separate files. Everything is currently mashed into main.go.

### Json schema

Good ideas: 

- [https://brandur.org/elegant-apis]()
- [https://github.com/brandur/simple-schema]()
