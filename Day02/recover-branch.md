## Scenario -

# How to recover the deleted branch?

**Possible varities**

- Branch present in remote and deleted from local
    - `git pull origin <branch-name>`
- Branch deleted from remote but present in local
    - ` git push origin <branch-name>`
- Branch deleted from both places
    - We can `git reflog` to find the commit of that branch.
    - `git checkout -b <branch-name> <commit-id>`
    - Branch will created with that commit.