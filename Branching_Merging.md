## Branching and merging

Start working in a brand new branch.  This command is creating a new branch and check it out at once: `$ git checkout -b <new-branch> <existing-branch>`

Example:
```
$ git checkout -b dev master
$ git checkout -b signup-site dev
```

Push the branch to the remote repository
```
$ git push --set-upstream origin dev
$ git push --set-upstream origin pluralsight
```

Merge the current branch to the `master` branch: `$ git merge origin master`

Merge the work you've done in your own branch with an existing branch: `$ git merge --no-ff myfeature`

Delete a branch with this command: `git branch -d myfeature`