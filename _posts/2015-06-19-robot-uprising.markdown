---
layout: post
title:  "Meetup Notes: Robot Uprising"
date:   2015-06-19 19:00:00
categories: meetup progress
author: Austin Pray
---

[Meetup link for posterity.](http://www.meetup.com/Dallas-Web-Mobile-Development-Meetup/events/222899516/)

## Project-wide Updates

### Twitter

Follow us on Twitter: [@liveplantio](https://twitter.com/liveplantio). 

It will automatically tweet project updates from this website. I also hope to
use it to post videos and pictures from the meetups. We are also posting
content from the meetup over at
[#liveplant](https://twitter.com/hashtag/LivePlant).

<a class="twitter-timeline" href="https://twitter.com/liveplantio" data-widget-id="612145104459968513">Tweets by @liveplantio</a>
<script>!function(d,s,id){var js,fjs=d.getElementsByTagName(s)[0],p=/^http:/.test(d.location)?'http':'https';if(!d.getElementById(id)){js=d.createElement(s);js.id=id;js.src=p+"://platform.twitter.com/widgets.js";fjs.parentNode.insertBefore(js,fjs);}}(document,"script","twitter-wjs");</script>

### Newsletter

I created a mailing list so you guys can get notified when a new about.liveplant.io project update is posted. Go ahead and sign right up below! It should be one email per week delivered on Mondays.

<!-- Begin MailChimp Signup Form -->
<link href="//cdn-images.mailchimp.com/embedcode/classic-081711.css" rel="stylesheet" type="text/css">
<style type="text/css">
	#mc_embed_signup{background:#fff; clear:left; font:14px Helvetica,Arial,sans-serif; }
	/* Add your own MailChimp form style overrides in your site stylesheet or in this style block.
	   We recommend moving this block and the preceding CSS link to the HEAD of your HTML file. */
</style>
<div id="mc_embed_signup">
<form action="//liveplant.us11.list-manage.com/subscribe/post?u=38fc17deee18f14fa02387f3b&amp;id=f986780b5a" method="post" id="mc-embedded-subscribe-form" name="mc-embedded-subscribe-form" class="validate" target="_blank" novalidate>
    <div id="mc_embed_signup_scroll">
	<h2>Get Liveplant Project Updates</h2>
<div class="indicates-required"><span class="asterisk">*</span> indicates required</div>
<div class="mc-field-group">
	<label for="mce-EMAIL">Email Address  <span class="asterisk">*</span>
</label>
	<input type="email" value="" name="EMAIL" class="required email" id="mce-EMAIL">
</div>
<div class="mc-field-group">
	<label for="mce-FNAME">First Name </label>
	<input type="text" value="" name="FNAME" class="" id="mce-FNAME">
</div>
<div class="mc-field-group">
	<label for="mce-LNAME">Last Name </label>
	<input type="text" value="" name="LNAME" class="" id="mce-LNAME">
</div>
	<div id="mce-responses" class="clear">
		<div class="response" id="mce-error-response" style="display:none"></div>
		<div class="response" id="mce-success-response" style="display:none"></div>
	</div>    <!-- real people should not fill this in and expect good things - do not remove this or risk form bot signups-->
    <div style="position: absolute; left: -5000px;"><input type="text" name="b_38fc17deee18f14fa02387f3b_f986780b5a" tabindex="-1" value=""></div>
    <div class="clear"><input type="submit" value="Subscribe" name="subscribe" id="mc-embedded-subscribe" class="button"></div>
    </div>
</form>
</div>
<script type='text/javascript' src='//s3.amazonaws.com/downloads.mailchimp.com/js/mc-validate.js'></script><script type='text/javascript'>(function($) {window.fnames = new Array(); window.ftypes = new Array();fnames[0]='EMAIL';ftypes[0]='email';fnames[1]='FNAME';ftypes[1]='text';fnames[2]='LNAME';ftypes[2]='text';}(jQuery));var $mcj = jQuery.noConflict(true);</script>
<!--End mc_embed_signup-->

## Robot Updates

Zach Stokes (@DeftxPunk) Brought some hardware in to hack on!

<blockquote class="twitter-tweet" lang="en"><p lang="und" dir="ltr"><a href="https://twitter.com/ChicagoGupta">@ChicagoGupta</a> <a href="https://twitter.com/hashtag/LivePlant?src=hash">#LivePlant</a> <a href="http://t.co/VH77gGjSRZ">pic.twitter.com/VH77gGjSRZ</a></p>&mdash; Austin Pray (@AustinPray) <a href="https://twitter.com/AustinPray/status/612061473473327104">June 20, 2015</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

![Box of goodies](http://i.imgur.com/fiNZkXp.jpg)

![Zach doing work](http://i.imgur.com/xQWQ6dg.jpg)

The microcontroller being used here is an MSP430 (the Texas Instruments flavor
of MCU). However, at this point I don't think anyone is particularly married to
any platform seeing as though no actual code has been written or hardware
constructed. We are hoping to change this very soon. 

Check out some discussion happening over [here](https://github.com/liveplant/liveplant-bot/issues/5)

## Server Updates

Check [the 1.0.0
milestone](https://github.com/liveplant/liveplant-server/milestones/1.0.0) for
current action items. The talented Shawn Spencer (@smspence) went ahead and
knocked out a basic prototype of the voting endpoint. You can take a look at
his handiwork [here](https://github.com/liveplant/liveplant-server/pull/19).

For people looking to jump in: definitely stop by
[gobyexample.com](https://gobyexample.com/) for a basic idea of how to start
slinging some Go.

I also set up a [wiki](https://github.com/liveplant/liveplant-server/wiki) over
on the GitHub repo so people can document their tips and tricks. I am
especially interested in people documenting how they set up a development
environment in Windows. I started a page for that over [here](https://github.com/liveplant/liveplant-server/wiki/Development-on-a-Windows-PC).

## Client Updates

Go ahead and start familiarizing yourself with [Ember][]. There is a getting started guide [here](http://guides.emberjs.com/v1.12.0/getting-started/).

[Ember]: http://emberjs.com/
