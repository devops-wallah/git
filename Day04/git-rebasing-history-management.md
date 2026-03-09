# 3. Git Rebasing & History Management

1. What is interactive rebase?
    - Used to change the history of existing commits, just run ` git rebase -i <commit-hash>` and change `pick` to -
    - Changing commit msg `reword`
    - Squashing commit - `squash`   
    - Edit commit content - `edit`
    - Delete commit - `drop`

2. How do you squash commits?
    - changing `pick` to `squash`

3. What is the difference between `git reset` and `git revert`?
    - reset delete the commit history
    - reset keep history and revert the change.

4. Explain `git reset --soft`, `--mixed`, and `--hard`.
    - `--soft` bring commit into stage and keep work area
    - `--mixed` bring chnages in work area, stage lost
    - `--hard` delete all areas and commit changes

5. When should you use `git revert` instead of `git reset`?
    - When we ant to preserve the commit history.

6. How do you remove a commit from history?
    - `git rebase -i` with drop

7. What is `git cherry-pick`?
    - Used to bring only specifc commits to branch.

8. What is `git reflog` and how is it used?
    - It store the changes we made to local repo
    - Helpfull to recover deleted commits, branches

9. How do you recover a deleted branch?
    - Get the last know commit of that branch using reflog
    - git checkout -b branch commit-hash

10. How do you recover lost commits?
    - again reflog 