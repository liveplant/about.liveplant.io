---
layout: post
title:  "Meetup Notes: Live Coding Session"
date:   2015-06-26 19:00:00
categories: meetup progress
author: Austin Pray
---

[Meetup link for posterity](http://www.meetup.com/Dallas-Web-Mobile-Development-Meetup/events/222229852/)

Today we did some live coding with the goal of getting familiar with the full
stack of technologies that will run liveplant.

<blockquote class="twitter-tweet" lang="en"><p lang="en" dir="ltr">Probably the dumbest picture ever taken <a href="http://t.co/rjMnXQwSPb">pic.twitter.com/rjMnXQwSPb</a></p>&mdash; Liveplant.io (@liveplantio) <a href="https://twitter.com/liveplantio/status/614608760162488320">June 27, 2015</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

## Javascript Live Coding

We ran through a minimal example of calling a REST API and adding the contents
of the request to the page.

### Demo

<iframe width="100%" height="300" src="//jsfiddle.net/austinpray/1enso59z/embedded/result,js,html" allowfullscreen="allowfullscreen" frameborder="0"></iframe>

### Concepts explored here

- Using [Bootstrap][] to save time styling
- Using jQuery to [add click handlers to DOM elements][jQuery click]
- Using jQuery to [make calls to a REST API][jQuery REST]
- [Adding output to the DOM][add to dom]

## Server Live Coding

For part two we explored the actual code that runs the REST endpoint we called
in the client side live coding demo. [Here is the code we went over][main.go].
We are focusing on the code that runs the [GET /current_action][current_action] endpoint.

To familiarize yourself with [go][] I highly recommend checking out [go by
example][gobyexample].

### [Constants](https://github.com/liveplant/liveplant-server/blob/3eb2cec49844b769f1328e7406598c8ebe8b0df6/main.go#L16-L21)

If ever we decide we want to change the literal string we use to identify an
action we can do it in one place rather than find and replace across the whole
project. [Learn more about constants](https://gobyexample.com/constants).

{% highlight go %}
// Define string constants that correspond
// to each supported action here
const (
	ActionWater   string = "water"
	ActionNothing string = "nothing"
)
{% endhighlight %}

### [Structs](https://github.com/liveplant/liveplant-server/blob/3eb2cec49844b769f1328e7406598c8ebe8b0df6/main.go#L32-L35)

We define a CurrentAction type so we can easily encode our data to JSON as well
as provide some structure to our responses.  [Learn more about structs](https://gobyexample.com/structs).

{% highlight go %}
type CurrentAction struct {
	Action        string `json:"action"`
	UnixTimestamp int64  `json:"unixTimestamp"`
}
{% endhighlight %}

{% highlight go %}
someVar := &CurrentAction{}
// => Action is empty string and UnixTimestamp is 0
{% endhighlight %}

<iframe 
  src="https://play.golang.org/p/XI3wX5aPLv" 
  frameborder="0" 
  style="width: 100%; height: 250px;"><a href="https://play.golang.org/p/XI3wX5aPLv">see this code in play.golang.org</a></iframe>

### [The `GET /current_action` handler function](https://github.com/liveplant/liveplant-server/blob/3eb2cec49844b769f1328e7406598c8ebe8b0df6/main.go#L37-L43)

This is a function that takes a http.ResponseWriter and writes some JSON to it.
If that doesn't make sense: just think of the `w` function argument as the
output.

- [Learn more about functions](https://gobyexample.com/functions)
- [Learn more about encoding JSON](https://gobyexample.com/json)
- [Learn more about http.ResponseWriter](https://golang.org/pkg/net/http/#ResponseWriter)

{% highlight go %}
func GetCurrentAction(w http.ResponseWriter, r *http.Request) {
	action := &CurrentAction{
		Action:        ActionWater,
		UnixTimestamp: int64(time.Now().Unix()),
	}
	json.NewEncoder(w).Encode(action)
}
{% endhighlight %}

Bonus knowledge: [to make a function public you capitalize the first letter of
the name. Otherwise it is
private](https://golang.org/ref/spec#Exported_identifiers). Thanks to @smspence
for figuring that out.

### [The router](https://github.com/liveplant/liveplant-server/blob/3eb2cec49844b769f1328e7406598c8ebe8b0df6/main.go#L139)

Ok so all the way up to this point we have done nothing but setup. We have only
defined a function but never called it. How does it get triggered? We use
[mux][] as our router. The name is pretty intuitive: we are "routing" our
request (`/current_action`) to it's corresponding handler function that
generates the output.

- [Learn more about mux][mux]

{% highlight go %}
func (app *Application) mux() *gorilla_mux.Router {
	router := gorilla_mux.NewRouter()

	router.HandleFunc("/current_action", GetCurrentAction).Methods("GET")
	router.HandleFunc("/votes", PostVotes).Methods("POST")
	router.HandleFunc("/votes", GetVotes).Methods("GET")

	return router
}
{% endhighlight %}

### And that's about it.

At this point you should be able to fiddle around with the code. [Go take a
crack at it.](https://github.com/liveplant/liveplant-server)

We are hoping to have some better instructions on running the development
environment merged soon. [Here is the work in
progress.](https://github.com/liveplant/liveplant-server/pull/22)

## In closing

Definitely interested in your feedback on the live coding stuff. I definitely
liked actually writing code rather than just talking about writing code.

[Bootstrap]: http://getbootstrap.com/
[add to dom]: https://api.jquery.com/jquery/#jQuery-element
[current_action]: https://liveplant.herokuapp.com/current_action
[go]: https://golang.org/
[gobyexample]: https://gobyexample.com/
[jQuery REST]: https://api.jquery.com/jQuery.get/
[jQuery click]: https://api.jquery.com/on/
[main.go]: https://github.com/liveplant/liveplant-server/blob/3eb2cec49844b769f1328e7406598c8ebe8b0df6/main.go
[mux]: http://www.gorillatoolkit.org/pkg/mux
