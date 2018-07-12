## Git Command Line Samples

### Essential Git Commands

Create a local clone of your fork  
 `$ git clone https://github.com/YOUR-USERNAME/Spoon-Knife`

View current configured remote repository  
`$ git remote -v`

Add remote repository  
`$ git remote add upstream https://github.com/octocat/Spoon-Knife.git`

Commit  
`$ git commit -a -m"The commit message"`

`Push` update the server with your commits across all branches that are *COMMON* between your local copy and the server.  Local branches that were never  pushed to the server in the first place are not shared.  
`$ git push`

Update the server with your commits made to `<branch>` since your last push. This is always *required* for new branches that you wish to share. After the first explicit push, `git push` by itself is sufficient.  
`$ git push origin <branch>`

Check if everything has been added or if you missed anything. Show files added to the staging area, files with changes, and untracked files  
`$ git status`  

`Pull` is a combination of the commands `fetch` and `merge`, so there may be merge conflicts to be manually resolved.  
`$ git pull upstream master`


---
### Syncing a fork

* You will use `upstream` to __fetch from the original repo__ (in order to keep your local copy in sync with the project you want to contribute to). Fetch the branches and their respective commits from the `upstream` repository. Commits to `master` will be stored in a local branch, `upstream/master`.  
`$ git fetch upstream`

* Check out your fork's local `master` branch.  Make the current branch `master`, updating the working directory to reflect the version referenced by `master`  
`$ git checkout master`

* Merge the changes from `upstream/master` into your local `master`  branch. This brings your fork's `master` branch into sync with the upstream repository, without losing your local changes.  
`$ git merge upstream/master`


---
### Stashing your code

You got a cool new idea and start working on it. You modify some files. You are not yet done, and your changes not even compile yet. Meanwhile you read on the mailing list that someone has got a problem with a specific test case and cannot get it to work. You would like to help because you know things like these very well. But what to do with your non finished code? Stash it away!  
`$ git stash topic_XY`

Git saves away your changes and your working copy is clean and compiles again. Now you fix the bug for your friend, commit the fix and publish it to your fork where others can access it. Now you can apply your saved away changes and continue working on it:
`$ git stash apply topic_XY`


---
### __Delete the last commit__

If the branch _master_ checked out locally
1. reset the branch to the parent of the current commit: `git reset HEAD^ --hard`
2. force-push it to the remote: `git push origin -f`

#### Explanation  
Let's say we have a remote _origin_ repository with branch _master_ that currently points to commit _dd61ab32_.  

We want to remove the top commit.  
Translated to git terminology: we want to force the remote _origin_ repository with branch _master_ to the parent of _dd61ab32_

`git push origin +dd61ab32^:master`

Where git interprets `x^` as the parent of `x` and `+` as a forced non-fastforward push.

#### References
* [Revert the full commit](https://gist.github.com/gunjanpatel/18f9e4d1eb609597c50c2118e416e6a6)
 * [Git HowTo: revert a commit already pushed to a remote repository](http://christoph.ruegg.name/blog/git-howto-revert-a-commit-already-pushed-to-a-remote-reposit.html)
