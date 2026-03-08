# Scenarios based on Branch and Merge

1. How do you rebase a feature branch onto the main branch?
    - We can use the `git rebase` cmd
    - Let's say you have main branch which has 5 commits and you created a new branch from it for feature-login
    - After few days, other developer opned and merged their changes to main.
    - Now main has 8 commits, but you branch don't have those changes in your local as well as in remote branch
    - you can bring those changes on your branch by rebasing it.

    How to do it?

    - Switch to main and pull the changes
    - Switch back your feature-login branch 
    - Run `git rebase main`
    - All changes from main are now present on feature-login branch

2. You want to merge only a specific commit from another branch. How do you do that?
    - `git log --oneline` get the commit id.
    - checkout or switch to required branch and run `git cherry-pick <commit-id>`
    - This will add that commit to the branch.

3. How do you delete a remote branch that is no longer needed?
    - `git push --delete origin <branch-name>`

4. Your main branch is ahead of your local branch. How do you update your branch without affecting your commits?
    - Make use of `rebase`
    - Pull changes from remote to main branch 
    - Switch to feature branch and run `git rebase main`
    - This brings all commits from main to feature branch.

5. What happens if you try to merge a branch that has already been merged?
    - Git will say `Already up to date.`

6. What is the difference between git merge and git rebase? When would you use each?
    - `git merge`
        - Merge will merge to branches in one with one extra commit i.e merge commit
        - Mostly used in enterprise.
    - `git rebase`
        - Rebase will bring the commits from one branch to another branch with updated commit id.
        - This will not add extra commit.     

7. A merge conflict occurs while merging a feature branch into main. How do you resolve it?
    - Make the changes in files which casuing conflit in local
    - Commit changes (conflict resolved). Push changes.