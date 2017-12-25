CPAN PR Challenge - 01/2015
2015-01-17T16:50:08Z

When I was reading through [Perl Weekly](http://perlweekly.com/) newsletter the other day, I realized that there is a challenge named 'CPAN Pull Request Challenge'. Everyone was invited to join, and I decided to give it a go. It was organized by Neil Bowers, who explained the details right [here](http://neilb.org/2014/11/29/pr-challenge-2015.html).

The idea was simple: For each month in 2015, each participant will be assigned a CPAN module. Then they will be asked to contribute to the code. Be it improving documentation, writing more tests to improve test coverage, fixing a bug or actually implementing a new feature, you were to do something and then submit a pull request on GitHub. As this challenge was open to 'anyone', there were several documents explaining how GitHub works, and how to submit your first pull request and what not. If you have a look at [blogs.perl.org](http://blogs.perl.org), you'll see several of them. Even if you're not going to participate, they are still pretty decent how-to documents, and having a look will not hurt.

Here's what I did for January: I was assigned [Exporter::Declare](https://github.com/exodist/Exporter-Declare), a module that is rather decent and in a good shape. First thing I realized was the readme file. It did not contain any markdown elements of GitHub. So I forked the code, renamed README to README.md (to denote markdown, explanation [here](http://stackoverflow.com/questions/5922882/what-file-uses-md-extension-and-how-should-i-edit-them)) and changed the file. I added headers, code blocks with syntax highlighting, and sent a [pull request](https://github.com/exodist/Exporter-Declare/pull/9).

![](images/cpanprc-oldreadme.png)
<div class="caption">Old readme file with no markdown.</div>

![](images/cpanprc-newreadme.png)
<div class="caption">Modified readme file with markdown.</div>

This was pretty simple and extremely easy task to complete, but it wasn't the great PR, as the readme file turned out to be auto generated. Then I took a look into [this post](http://blogs.perl.org/users/michal_wojciechowski/2011/11/github-friendly-readme-files-with-extutils-makemaker-and-module-build.html), which described the way to handle auto-generated github-friendly readme files. I ended up creating another pull request for this approach at [here](https://github.com/exodist/Exporter-Declare/pull/10).

![](images/cpanprc-autoreadme.png)
<div class="caption">Automatically generated readme file with markdown.</div>

It's a small contribution, but I believe it's still better than giving nothing to the community at all. Plus, this is only the beginning. There will be 11 more tasks assigned to me, and I promise to work harder on upcoming module assignments. For example, I haven't written any tests for my only module on CPAN, as I always found an excuse to skip writing them. As searching for what I can do to improve my assignment, I've already learned about [Devel::Cover](http://blogs.perl.org/users/neilb/2014/08/check-your-test-coverage-with-develcover.html), [cpancover.com](http://cpancover.com), and [cpantesters](http://www.cpantesters.org/). Test is not the only thing I've learned about: There is [Perl::Critic](http://en.wikipedia.org/wiki/Perl::Critic) that evaluates your code. There is also a way to [add your github link to the meta file](http://perlmaven.com/how-to-add-link-to-version-control-system-of-a-cpan-distributions).

I'll finish with two quotes: One is about pull requests. They say that the 'true' way of submitting a PR is by [creating a new branch](http://neilb.org/2015/01/10/pr-in-branch.html). This was something I was not aware of. The other one comes from the mail-list of CPAN-PR: They say "Code can almost always use more comments: this is no exception."

If you want to join in, I suppose you're not late. Try to e-mail Neil Bowers and he'll most probably assign you a module. See January assignments [here](http://cpan-prc.org/2015/january.html) (not all of them are public, so the number is higher than what you see.)
