## Git Command Line Samples

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

 ---

Create a local clone of your fork  
 `$ git clone https://github.com/YOUR-USERNAME/Spoon-Knife`

View Current Configured remote repository  
`$ git remote -v`

Add remote repository
`$ git remote add upstream https://github.com/octocat/Spoon-Knife.git`


### Syncing a fork

* You will use `upstream` to __fetch from the original repo__ (in order to keep your local copy in sync with the project you want to contribute to). Fetch the branches and their respective commits from the `upstream` repository. Commits to `master` will be stored in a local branch, `upstream/master`.  
`$ git fetch upstream`

* Check out your fork's local `master` branch.  
`$ git checkout master`

* Merge the changes from `upstream/master` into your local `master`  branch. This brings your fork's `master` branch into sync with the upstream repository, without losing your local changes.  
`$ git merge upstream/master`

