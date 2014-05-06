learngit
========

1. Forking (once per project)
--------
Click on the 'Fork' button in the top right there. This will 'fork' the repo to your account. That means you have your own copy of this project which you can do whatever you like with.

2. Cloning your fork (once per project)
--------

Navigate to your fork on github (http://github.com/youraccountname/learngit

Copy the SSH clone URL in the right hand bar.

On the command line, cd to the directory you want to clone it to and run this:

```git clone PASTE_SSH_URL_HERE```

This will create a folder in that directory called 'learngit' with your copy of the project in it. Note this is from your fork, not the main one!


3. Adding a reference to the main repo (once per project)
--------

You'll need to add a reference to the main repo so you can keep up to date with any changes it makes. You only need to do this once:

Run this in your 'learngit' folder in your repo:

```git remote add upstream git@github.com:cham/learngit.git```

This will add a reference to a remote repo called 'learngit' to your local copy.

You can see all your remotes by running this:

```git remote -v```

The ones with (fetch) after are ones you can pull from and the ones with (push) after are ones you can push to.

You should have 2 entries for origin, fetch and push - because you own that one so you can do what you like with it - and at least a fetch entry for upstream.


4. Branching (once per feature / bugfix / whatever)
--------

First of all, checkout your master:

```git checkout master```

Then fetch the latest history from upstream, so you can apply that history to your master in a moment:

```git fetch upstream```

Once that's done you can rebase your local master against the upstream master. In other words, pull the latest changes and apply them to your master branch

```git rebase upstream/master```

Now you can make your branch, which will be based off the current branch (your master which you just updated):

```git checkout -b your-branch-name```


5. Working
--------

Do some work, edit files, etc. When you want to make a commit:

```git add -p```

This runs an interactive add which allows you to select which parts of which files you want to add to the commit.

When you're happy with what you've added check things are looking ok with:

```git status```

It should tell you the right files are staged for commit. If not you can 'git reset HEAD' which will unstage everything (but not delete anything)

Make your commit and give it a descriptive message:

```git commit -m "This fixes that bug!"```

And push it to your remote

```git push origin your-branch-name```

Now your local branch will be pushed up to your remote - you can see it on github if you go to https://github.com/youraccountname/learngit/branches


6. Submitting a PR
--------

Now your branch is uploaded to your origin (your fork), you can submit a PR for it so that it's included in the main repo.

Navigate to the main repo in your browser - https://github.com/cham/learngit

Click on the green PR button, near the top. There should be an entry there with your branch name on it if you just pushed it.

Github will let you review the PR before submitting, add a description, etc

Submit your PR

Wait for comments / merge!

