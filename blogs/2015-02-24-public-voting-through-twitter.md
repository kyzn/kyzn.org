Public Voting through Twitter
2015-02-24T12:50:01Z

Last week, we organized a charity party. It was more like a contest, or a show, in which 10 teams participated. Each team was supposed to perform a show on their choice: dance, music, or even a play. We also had a judge of 5 people to grade performances. These people were not the only ones to decide who wins the night, though. There was going to be a public voting, that anyone can participate.

So I wrote a Perl script for the party. We picked an event keyword starting with a # character, and listened Twitter for tweets including that word. Then, we had different keywords for each team. Anyone who wanted to cast their vote would just tweet with event keyword + team keyword, and that would be it.

![](images/votepl-ads.png)
<div class="caption">People asking their followers to vote for their teams</div>

We could have performed a basic search on Twitter Web, and then count the votes one by one, but that wouldn't be a smart solution. Hence the script. It was run for 15 minutes, and we captured 275 tweets with event hashtag which is about one tweet per 3 seconds. However, only 179 tweets were counted as 'valid vote', which is 65% of total tweets. But why did we ignore 96 tweets?

We've developed precautive measurements in the script so that no team can abuse the automated vote counting process. We did not count forwarded tweets (that is, a retweet), and there were 22 many. We counted only the first vote of each person. There were 32 tweets that had a note saying "This person has voted before!". We also checked for   age of each account. If the account the vote is casted from is newly created, we did not count the vote. If the tweet is sent from an unofficial application, we ignored. And 41 tweets did not contain any team keyword (or had typos in it).

Although tested heavily, I was scared that it simply wouldn't work for no obvious reason. But it did! And it did a good job. The script is on [GitHub](http://github.com/kyzn/twitter-voting), you can use it as you wish.
