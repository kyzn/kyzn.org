Two Perl Conferences in One Year
2018-08-20T12:00:00Z

My very first Perl Conference was the one in Orlando, in 2016. In fact, the only blog I've written in 2016 was about that very conference. I've enjoyed it so much, I went again in 2017, this time as a speaker.

I have attended not one but two Perl Conferences during 2018: One in Salt Lake City (NA), and one in Glasgow (EU). This time I was not only a speaker: I also organized a Birds of Feather (BOF). My talks and BOFs were about CPAN Pull Request Challenge.

How many Perl Conferences is too many Perl Conferences, that I still don't know. But I can say I enjoyed both conferences a lot. Here's some takeaways, with a focus on talks I did.

## Importance of Ecosystem

VM Brasseur gave a keynote on a very serious topic in Salt Lake City. It was about being inclusive and not being harmful. I recommend everyone to watch it, and think about their environment while doing so.

<iframe width="100%" height="315" src="https://www.youtube.com/embed/ySWez59lhH0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

This talk inspired me to build a Dist::Zilla plugin to make it easy to add a Code of Conduct to CPAN modules. The idea was that you could add one line to your dist.ini file, and get a Code of Conduct.

I gave a lightning talk about this very module in Glasgow. I'm glad I did that because it lead to a very constructive discussion. I already have a [plan](https://github.com/kyzn/Dist-Zilla-Plugin-ContributorCovenant/issues/3) to improve it. This was another proof for me that keeping in touch with your community matters. Presenting your ideas matters. Providing constructive critisism _and_ listening to it matters.

There were more great talks given on the topic. Do you want to hear about how to make your application more inclusive? Then you should see Joelle Maslak's talk "[You're not wanted here](https://www.youtube.com/watch?v=ZqpCKisOL5k)". Do you want to get some crucial tips on how to make your community more friendly? Then you should also see Ruth Holloway's "[Discourse without drama](https://www.youtube.com/watch?v=-lWnmVm5owQ)". Both speakers delivered their talks at both venues.

I am also going to recommend "[Developers, engineers and the downward spiral](https://youtu.be/RfdOYbyRwB4?t=3h13m40s)" by Christopher Rasch-Olsen Raa, given in Glasgow. This talk has very important notes about mental health. You will find some crucial tips for employees, managers, and leaders.

## Pull Request Challenge

Neil Bowers is organizing Pull Request Challenge for 4 years now. In January 2018, he announced that it is going to [end this year](http://neilb.org/2018/01/01/cpan-prc-2018.html). I'm trying to build a successor named [pullrequest.club](https://pullrequest.club).  I've presented a talk that explained what Pull Request Challenge is in general.


<iframe width="100%" height="315" src="https://www.youtube.com/embed/QiZOEIwkuek" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

Mohammad Anwar gave a great talk on how to become a CPAN contributor. I recommend this talk to everyone, but especially to people who feel that "their code is not good enough".  He will tell you why you don't have to be an expert to contribute! If this sounds like a joke to you, it's not. You really don't have to be an expert. He will also tell you about the self-confidence boost you'll get when your PR gets merged.

<iframe width="100%" height="315" src="https://www.youtube.com/embed/QYN1nijo9VY" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Some Notes

- You can suppress that long output you get when using `reply` by adding `1` to the end. Instead of `$schema->resultset('Child')`, do a `$schema->resultset('Child'); 1`! (The Perl Advent Calendar 2017 Redux, Mark Fowler, Glasgow)
- Term::Choose is a cool alternative to Getopt::Args. It prints options to terminal, through which user navigates with arrow keys. (The Perl Advent Calendar 2017 Redux, Mark Fowler, Glasgow) 
- The Perl Advent Calendar is accepting submissions for 2018 edition! Go to [cfp.perladvent.org](http://cfp.perladvent.org/) if interested. (LT Advertisement, Mark Fowler, Glasgow)
- 101 year old people use computers too! (Joelle Maslak, You're Not Wanted Here, Salt Lake City)
- When writing tests, make sure it fails first. Tests are code too, so don't ignore the fact that they might contain bugs. (Scott Lee, Writing Testable Code, Salt Lake City)
- `.dockerignore` is much like `.gitignore`. It ignores files listed in it when doing a copy command for docker. (Wesley Schwengle, Docker for Perl Developers, Glasgow)
- There is an open source network vulnerability scanner named [Arachni](https://github.com/Arachni/arachni) and it's pretty good. (Lee Johnson, Find and fix your web security vulnerabilities with Burp Scanner, Glasgow)

That's all for now! See you all next time.
