# Advanced Git Scenarios

1. Explain the difference between git revert and git reset. When would you use each?
    - `git revert`
        - This will keep the commit history.
        - If we revert, we will create new commit to push.
    - `git reset`
        - This delete the commit from history. 
        - Used when you want to make changes to same commit again.

2. You need to squash multiple commits into one before pushing. How do you do that?
    - To Squash on local, we need to use `git rebase -i HEAD~n`
    - change the `pick` to `squash` then save. add final commit.

3. How do you rewrite commit history to change a commit message from a few commits ago?
    - `git rebase -i commit-id `
    - change `pick` to `reword` then save

4. Explain how git cherry-pick works and when you would use it.
    - If you want bring specific commits to branch then we can use cherry-pick.
    - e.g If we want to deploy only spcific feature from dev and qa to prod.

5. How do you create and apply patches in Git?
    - In Git, patches are used to share changes as a file instead of pushing to a remote repository. Another developer can apply those changes to their repository.
    - This is useful when:
        No direct repo access
        Sending fixes via email
        Contributing to open-source projects
        Code review workflows

6. You have diverged from the remote branch, and your local commits conflict with remote changes. How do you fix this?
    - First pull remote branch then rebase local branch with it.
    - Fix conflicts and commit.

7. You need to find out who made changes to a specific line in a file. What command do you use?
    - Using `git blame`

8. How do you temporarily save changes that are not ready to be committed?
    - `git stash` to put changes to stash 
    - `git stash apply stash@{id}` to bring back changes

9. Your Git repository has become very large. How do you reduce its size without affecting its history?
    - Using garbage collectiion to remove dangling commits.
    - If a Git repository becomes large and we want to reduce its size without changing history, we can run git gc to clean unused objects and repack the repository. We can also prune stale remote references using git remote prune, expire reflog entries, and run git gc --aggressive --prune=now to optimize storage while keeping the commit history intact.