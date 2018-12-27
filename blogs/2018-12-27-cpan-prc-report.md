CPAN-PRC Report
2018-12-27T12:00:00Z

Neil Bowers had started CPAN Pull Request Challenge in January 2015. Participants received a CPAN module as their assignment each month. The goal was to submit pull requests. I joined the challenge right away. Here's how it went.

## 2015: Warming Up

My last semester at Bogazici University in Istanbul started February of this year. I moved to California for grad school in September.

I’ve completed my assignments in January and February before taking a long pause (and a long flight). I’ve joined back for October and November. 6 PRs for 4 repos, only 1 merged. All were either documentation updates or configuration changes.

| ---- | --- | ------------- | ------ | --------------------------- |
| 2015 | Jan | Documentation | CLOSED | Exporter-Declare            |
| 2015 | Jan | Documentation | MERGED | Exporter-Declare            |
| 2015 | Feb | Config        | OPEN   | Dancer-Plugin-Auth-Basic    |
| 2015 | Oct | Config        | OPEN   | HTML-FormHandler-Model-DBIC |
| 2015 | Oct | Config        | OPEN   | HTML-FormHandler-Model-DBIC |
| 2015 | Nov | Documentation | OPEN   | HTML-StickyQuery-DoCoMoGUID |

## 2016: See if I can fix this

I graduated from Santa Cruz and relocated to Santa Monica for ZipRecruiter. This was my first job, excluding some internships I did back at Istanbul. Attended my first Perl Conference in June in Orlando.

Like in 2015, I did my assignments only for 4 months. This time I tried to fix some failing tests too. Results were great: 4 PRs, 4 merged!

| ---- | --- | ------------- | ------ | -------------------------------------- |
| 2016 | Jun | Documentation | MERGED | HiD                                    |
| 2016 | Oct | Test          | MERGED | Catalyst-Controller-Validation-DFV     |
| 2016 | Nov | Test          | MERGED | BenchmarkAnything-Storage-Frontend-Lib |
| 2016 | Dec | Test          | MERGED | Monitoring-Livestatus                  |

## 2017: More Pull Requests

This year was fun: I completed 8 assignments with 13 PRs with 7 merged. It was a mix of documentation, configuration, test fixes and new functions. We have started to get “team assignments” for ZipRecruiter as well, which is not included in this post.

| ---- | --- | ------------- | ------ | ------------------------- |
| 2017 | Jan | Config        | MERGED | Devel-ebug                |
| 2017 | Feb | Function      | MERGED | Log-Dispatch              |
| 2017 | Mar | Function      | MERGED | Mail-Builder              |
| 2017 | Mar | Test          | MERGED | Mail-Builder              |
| 2017 | May | Function      | MERGED | AnyEvent-WebSocket-Client |
| 2017 | Jun | Config        | OPEN   | Net-Proxy                 |
| 2017 | Jul | Test          | CLOSED | Class-Inspector           |
| 2017 | Jul | Config        | MERGED | Class-Inspector           |
| 2017 | Aug | Config        | OPEN   | App-p                     |
| 2017 | Aug | Documentation | OPEN   | App-p                     |
| 2017 | Aug | Config        | OPEN   | App-p                     |
| 2017 | Aug | Function      | OPEN   | App-p                     |
| 2017 | Oct | Function      | MERGED | AnyEvent-Filesys-Notify   |


## 2018: This is the end

Neil let us know that this will be the end of CPAN Pull Request Challenge. I was able to complete my assignment only for 5 months with 6 PRs and 4 merged.

I gave talks about CPAN Pull Request Challenge & [Pull Request Club](https://pullrequest.club) in two conferences. Salt Lake City (Perl Conference in NA) and Glasgow (Perl Conference in EU). We also had BOF (Birds of Feather) events for pull requests in both venues. Many people, whom I am thankful for, had showed up and contributed to open source. Some people submitted their first public PR, which made it a magical moment.

| ---- | --- | ------------- | ------ | -------------------- |
| 2018 | Jan | Config        | MERGED | Net-DHCP             |
| 2018 | Feb | Config        | MERGED | Alien-LibGumbo       |
| 2018 | Aug | Config        | MERGED | Text-CSV             |
| 2018 | Oct | Documentation | CLOSED | Data-DPath           |
| 2018 | Nov | Documentation | OPEN   | Vim-Debug            |
| 2018 | Nov | Config        | MERGED | Text-MediawikiFormat |

Did you see a pattern? I never missed any October! This is all thanks to Hacktoberfest.

![](images/hacktoberfest.jpg)

## Total Stats

I played with this data a little, and out came an interesting result: I've got 56% merge rate. This goes way up to 80% for function/test changes, and down to 29% for documentation. Here's all numbers.

|        | Config |  Doc  | Function | Test  |  TOTAL |
| ------ | ------ | ----- | -------- | ----- | ------ |
| Open   |    6   |   3   |    1     |   -   |   10   |
| Closed |    -   |   2   |    -     |   1   |    3   |
| Merged |    6   |   2   |    4     |   4   |   16   |
| TOTAL  | __12__ | __7__ |  __5__   | __5__ | __29__ |

And here is a breakdown by status (open, closed or merged), for each type (config, doc, etc). Each column adds up to 100%.

|        |  Config |   Doc   | Function |  Test   | All Types |
| ------ | ------- | ------- | -------- | ------- | --------- |
| Open   |   50%   |   42%   |   20%    |    -    |    34%    |
| Closed |    -    |   29%   |    -     |   20%   |    10%    |
| Merged | __50%__ | __29%__ | __80%__  | __80%__ |  __56%__  |

## Thanks

Thanks a lot to Neil Bowers for organizing the challenge and inspiring many people. Thanks a lot to all participants for keeping it alive. Thank you for reading!

If you were a participant of CPAN-PRC and want to keep going, give [Pull Request Club](https://pullrequest.club) a try. We currently have 14 participants and 120 repos ready for a match.
