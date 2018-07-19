## Syncing an upstream repository into your fork

* You will use `upstream` to __fetch from the original repo__ (in order to keep your local copy in sync with the project you want to contribute to). Fetch the branches and their respective commits from the `upstream` repository. Commits to `master` will be stored in a local branch, `upstream/master`.  
`$ git fetch upstream`  
`git fetch` only downloads new data from a remote repository - but it doesn't integrate any of this new data into your working files. Fetch is great for getting a fresh view on all the things that happened in a remote repository. `fetch` will never manipulate, destroy, or screw up anything.

* Check out your fork's local `master` branch.  Make the current branch `master`, updating the working directory to reflect the version referenced by `master`  
`$ git checkout master`

* Merge the changes from `upstream/master` into your local `master`  branch. This brings your fork's `master` branch into sync with the upstream repository, without losing your local changes.  
`$ git merge upstream/master`

---

### Syncing and merging an upstream repository into your fork

* Checkout the branch you wish to merge to.  Usually `master`  
  `$ git checkout <branch_name>`

* Pull the desired branch from upstream repository. This method will retain the commit history without modification.
`$ git pull --ff-only https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git <branch_name>`  

* Resolve any conflicts, if there are and commit the merge

* Push the merge to your GitHub repository  
  `$ git push origin <branch_name>`
