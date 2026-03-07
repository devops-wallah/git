#

## How to rebase the branch?


We can use the `git rebase` cmd

- Let's say you have main branch which has 5 commits and you created a new branch from it for feature-login
- After few days, other developer opned and merged their changes to main.
- Now main has 8 commits, but you branch don't have those changes in your local as well as in remote branch
- you can bring those changes on your branch by rebasing it.

How to do it?

- Switch to main and pull the changes
- Switch back your feature-login branch 
- Run `git rebase main`
- All changes from main are now present on feature-login branch
