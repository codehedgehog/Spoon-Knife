## Git Command Line Samples

### Essential Git Commands

Create a local clone of your fork  
 `$ git clone https://github.com/YOUR-USERNAME/Spoon-Knife`

View current configured remote repository  
`$ git remote -v`

Add remote repository / remote branch  
`$ git remote add upstream https://github.com/octocat/Spoon-Knife.git`

Commit  
`$ git commit -a -m"The commit message"`

`Push` update the server with your commits across all branches that are *COMMON* between your local copy and the server.  Local branches that were never  pushed to the server in the first place are not shared.  
`$ git push`

Update the server with your commits made to `<branch>` since your last push. This is always *required* for new branches that you wish to share. After the first explicit push, `git push` by itself is sufficient.  
`$ git push origin <branch>`

Check if everything has been added or if you missed anything. Show files added to the staging area, files with changes, and untracked files  
`$ git status`  

---

`Pull` is a combination of the commands `fetch` and `merge`, so there may be merge conflicts to be manually resolved.  
`$ git pull origin <branchname>` will get latest code for single branch which resides on the "origin" tree  
Example:   
`$ git pull upstream master`   

Basically:   
* `git pull` = `git fetch` + `git merge`  
* `git pull -r` = `git fetch` + `git rebase`

Using the `--rebase` flag will pop out your local changes, do a fast-forward to what the remote branch has, THEN place your commits on top.

To avoid messy merge commits and help keep a relatively clean git commit history use the following workflow when fetching upstream changes:
```
$ git fetch origin
$ git rebase −p origin/develop
```