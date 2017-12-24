How to Join #yapc on irc.perl.org
2017-06-19T03:18:10Z

 - IRC is used A LOT during The Perl Conference
 - To go online instantly in a browser, you can use [Mibbit](https://chat.mibbit.com/#yapc@irc.perl.org)
 - To stay online (to read all messages sent, even the ones sent when you were not around), you can use [IRCCloud](https://www.irccloud.com)
 - You can set up your own bouncer too!

<blockquote class="twitter-tweet" data-lang="en">
<p dir="ltr" lang="en">And if you are also headed to <a href="https://twitter.com/hashtag/tpc2017dc?src=hash">#tpc2017dc</a>, hop on <a href="https://t.co/2UAyAKRpW3">https://t.co/2UAyAKRpW3</a>#yapc and hang out with the cool kids! <a href="https://twitter.com/hashtag/tpc2017?src=hash">#tpc2017</a> <a href="https://twitter.com/hashtag/perl?src=hash">#perl</a></p>
— just john @ home. (@genehack) <a href="https://twitter.com/genehack/status/876059761657077760">June 17, 2017</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>
<blockquote class="twitter-tweet" data-lang="en">
<p dir="ltr" lang="en"><a href="https://t.co/ju5k4bqbD1">https://t.co/ju5k4bqbD1</a> channel <a href="https://twitter.com/hashtag/yapc?src=hash">#yapc</a> is a good place to community-coordinate beyond the wiki <a href="https://twitter.com/hashtag/tpc2017dc?src=hash">#tpc2017dc</a> <a href="https://t.co/hHjma16LlQ">https://t.co/hHjma16LlQ</a></p>
— Perl Conferences (@PerlConferences) <a href="https://twitter.com/PerlConferences/status/876570261444866049">June 18, 2017</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>



## Introduction

Last year's The Perl Conference at Orlando was my first one. I had a lot of fun, met with brilliant people and learned numerous things about Perl.

There was one thing that I didn't expect: People actually use IRC! Wiki for YAPC 2016 has a page named [Tips for First Timers](http://www.yapcna.org/yn2016/wiki?node=FirstTimers) which includes a note saying "Not All the Fun Happens in Meatspace". Indeed, IRC serves as a perfect medium for people to communicate, comment (on talks), ask for help, and so on.

If you are attending YAPC, and not reading #yapc, you are missing **a lot**.



## What is IRC anyway?

IRC stands for Internet Relay Chat.. and it's been around since 1988! It lets people communicate in real time (think ancestor of Slack). There are channels like #yapc in servers like irc.perl.org. <a href="https://en.wikipedia.org/wiki/Internet_Relay_Chat" target="_blank">Wikipedia</a> has a lot more details if you want to take a look.



## How do I get online now?

The fastest way to do it would be to use a service like [Mibbit](https://chat.mibbit.com/#yapc@irc.perl.org). You only need to pick a nickname, and you are online!

There are a ton of applications available. Take a look at [last year's wiki](http://www.yapcna.org/yn2016/wiki?node=IRC) to find what's best for you.

If you decide to connect through an app, you might need to set up a few more things. Here's a screenshot from HexChat:

![HexChat Configuration without bouncer](images/irc-hexchat-1.png)

Make sure address is `ssl.irc.perl.org/7062` (`irc.perl.org/6667` works too), enable SSL, pick a nickname and leave password blank. That's pretty much it!

There's a caveat though: You will be missing any messages sent when you are offline.



## So how do I stay online all the time?

You need a bouncer. Think of it as a middle-man: Bouncer connects to irc.perl.org on behalf of you, then you connect to your bouncer through your IRC client. Since the bouncer is always connected, you won't be missing any messages.

There is a service for that too, called [IRCCloud](https://www.irccloud.com). It has a free plan which is good for a week, except you still have to login every two hours or so. They also have Android and iOS apps.



## How do I set up my own bouncer?

If you have a machine running 7/24, or willing to fire up a DigitalOcean/Linode box, here's what you need to do:

 - `sudo apt-get install znc` ([more ways to install znc](http://wiki.znc.in/Installation)</a>)
 - znc won't work under root, so you need to have at least one non-root user. You can add one: `adduser znc && su znc && cd ~ `
 - `znc --makeconf`
    - **Listen on port:** This is tricky. If you are on a public wifi that blocks ports (could be the case for some conference venues) you need to make sure you pick a port that you have access to. Or you can use VPN to avoid that.
    - **Server host:** `ssl.irc.perl.org` (or `irc.perl.org`)
    - **Server uses SSL:** yes
    - **Server port:** 7062 (or 6667)
    - Server password is empty
    - **Initial channels:** #yapc (yay!)

![First part of znc setup](images/irc-znc-1.png)

![Second part of znc setup](images/irc-znc-2.png)

Once all is done, it will ask you whether you want to run znc now, which you can say yes. I also recommend setting a cronjob that restarts znc if it's not running for some reason.

`*/10 * * * * /usr/local/bin/znc >/dev/null 2>&1`

If you want to see the admin panel, you can go to https://host:port. (port that znc listens to). You can login with admin username & password you set during znc configuration setup.

Only thing left is to set up your client just like before.

![Hexchat configuration with bouncer](images/irc-hexchat-2.png)

 - Address is host/port
 - SSL is enabled
 - Username is admin_username/network_name (both set at znc config setup)
 - Login method is Server Password, and the password is admin password.

That's it! See you at #yapc!
