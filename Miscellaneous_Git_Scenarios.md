## Miscellaneous Git Scenarios

### Stashing your code

You got a cool new idea and start working on it. You modify some files. You are not yet done, and your changes not even compile yet. Meanwhile you read on the mailing list that someone has got a problem with a specific test case and cannot get it to work. You would like to help because you know things like these very well. But what to do with your non finished code? Stash it away!  
`$ git stash topic_XY`

Git saves away your changes and your working copy is clean and compiles again. Now you fix the bug for your friend, commit the fix and publish it to your fork where others can access it. Now you can apply your saved away changes and continue working on it:  
`$ git stash apply topic_XY`


---
### Revert to the last commit

Revert to the last commit
`$ git revert HEAD`

Revert to the next-to-last commit
`$ git revert HEAD^`

Revert your work to the desired commit
`$ git reset <commit_number>`

In case you wrongly added files to commit, use `git reset`  
For example: 
`$ git reset db/schema.rb` would remove this file from the files to be committed.

Delete files and remove them from the Git history
`$ git rm $(git ls-files –deleted)`


---

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
