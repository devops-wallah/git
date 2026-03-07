## 

# You commited changes to wrong branch, how to get those chnages to required branch?

**We can use `git cherry-pick` to achive this**
- Get the commit-id which need to move on branch using `git log --oneline`
- checkout the required branch `git checkout <branch-name>` or `git switch <branch-name>`
- Run `git cherry-pick <commit-id>`, commit moved to that branch
