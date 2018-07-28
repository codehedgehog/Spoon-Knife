### Well hello there!

This repository is meant to provide an example for *forking* a repository on GitHub.

Creating a *fork* is producing a personal copy of someone else's project. Forks act as a sort of bridge between the original repository and your personal copy. You can submit *Pull Requests* to help make other people's projects better by offering your changes up to the original project. Forking is at the core of social coding at GitHub.

After forking this repository, you can make some changes to the project, and submit [a Pull Request](https://github.com/octocat/Spoon-Knife/pulls) as practice.

For some more information on how to fork a repository, [check out our guide, "Forking Projects""](http://guides.github.com/overviews/forking/). Thanks! :sparkling_heart:

---
## Forking and Cloning

__[Fork](https://help.github.com/articles/fork-a-repo)__, in the GitHub context, doesn't extend Git.
It only allows clone on the server side.

When you clone a GitHub repo on your local workstation, you can only push changes to your own fork. You cannot contribute back to the upstream repo unless you are explicitly declared as "contributor". That's because your clone is a separate instance of that project. 

If you want to contribute to the project, you can use forking to do it, in the following way:
* clone that GitHub repo on your GitHub account (that is the ["fork" part](https://help.github.com/articles/fork-a-repo), a clone on the server side)
* contribute commits to that GitHub repo (it is in your own GitHub account, so you have every right to push to it)
* signal any interesting contribution back to the original GitHub repo (that is the __["pull request" part](https://help.github.com/articles/using-pull-requests)__ by way of the changes you made on your own GitHub repo)

If you want to keep a link with the original repo (also called upstream), you need to add a remote referring that original repo.

![fork and upstream](content/img/cEJjT.png)

---

* [Essentials Git Command](Essentials_Git_Commands.md)

* [Branching and Merging](Branching_Merging.md)

* [Syncing an upstream repository into your fork](Syncing_Upstream.md)
  * [Syncing and merging an upstream repository into your fork](Syncing_Upstream.md#syncing-and-merging-an-upstream-repository-into-your-fork)

* [Miscellaneous Git scenarios](Miscellaneous_Git_Scenarios.md)
  * [Stashing Your Code](Miscellaneous_Git_Scenarios.md#Stashing-Your-Code)
  * [Revert to the last commit](Miscellaneous_Git_Scenarios.md#Revert-to-the-last-commit)

---

### References:
* [Are git forks actually git clones?](https://stackoverflow.com/questions/6286571/are-git-forks-actually-git-clones)
* [Git Command Line Cheat Sheets](http://cheat.errtheblog.com/s/git) Comprehensive git command cheat sheets
* [Git Magic](http://www-cs-students.stanford.edu/~blynn/gitmagic/index.html) A good introduction to git
* [Pro Git](https://www.git-scm.com/book/en/v2It) Open source book about git.
* [Collaborative GitHub Workflow](http://www.eqqon.com/index.php/Collaborative_Github_Workflow)
