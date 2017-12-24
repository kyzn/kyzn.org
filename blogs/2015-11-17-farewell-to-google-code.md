Farewell to Google Code
2015-11-17T09:28:48Z

A while ago, Google decided to shut down Google Code, which [hosts over 200k projects](http://stackoverflow.com/a/8306775/1245539). It is in read-only status as of now. You cannot update your code any more. No more wiki updates or issues, it's gone. But, you can still reach the repositories and all pages, that's what they mean by read only. It is also noted that Google is [not going to delete your data](https://code.google.com/p/support/wiki/ReadOnlyTransition), just move it to ["Google Code Archive"](https://code.google.com/archive/).

If you decide to maintain your project, you should probably move your code, wiki and issues somewhere else. You might have already done this before, but here we go:

**Step 1: Export to GitHub**


 - Create a GitHub account if you don't have any.
 - Go to your Google Code or Google Code Archive page, click the button "Export to GitHub".
 - Authorize with your GitHub account, and it will do the magic.


![](images/google-code.png)
<div class="caption">See the button at right top?</div>

**Step 2: Where did my wiki go?**

Now you'll see a new repository on your GitHub account named exactly the same with your Google Code project. You'll see your code, your issues, but where is your wiki? Well, it exports your wiki as a new branch, not as a GitHub wiki. But that's not what you want? Don't worry, there's a quick fix for that: morgant@GitHub had written a script to convert that branch into an actual wiki. (It's actually one of the frequently asked questions, you can see all of them [here](https://code.google.com/p/support-tools/wiki/GitHubExporterFAQ), in case you have some other problem.)

 - Download the script [for OSX](https://raw.githubusercontent.com/morgant/finishGoogleCodeGitHubWikiMigration/master/finishGoogleCodeGitHubWikiMigration) and [for Linux](https://raw.githubusercontent.com/seraasch/finishGoogleCodeGitHubWikiMigration/master/finishGoogleCodeGitHubWikiMigration). See [readme](https://github.com/morgant/finishGoogleCodeGitHubWikiMigration) for details.
 - `chmod a+x finishGoogleCodeGitHubWikiMigration` (make it executable)
 - At GitHub repository, go to your project settings, mark the checkbox that says "Wikis".
 - Actually go to the wiki and create a page, usually done with few clicks.
 - Now run the script: `finishGoogleCodeGitHubWikiMigration https://github.com/<user>/<project>.git`
 - Review its commits. Only `git push` if you like the changes.
 - If you don't want to keep wiki branch: `git push origin :wiki`


Just as a note, I think it somehow exposes your html style comments if you had any. So you might want to remove them. Also, your sidebar might not show up. To solve this, I went to Google Code wiki, copied html source for the sidebar, replaced code google links with just the name of wiki page.

I think that's all! If you haven't moved your Google Code project yet, today's the day.
