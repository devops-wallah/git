# Basic Git Scenarios

1. You accidentally committed sensitive credentials in Git. How do you remove them from history?
    - We can use `git filter-repo` utility.
    - This is not coming as built in.
    - Install using `pip install git-filter-repo`
    - To remove specific secret use - `git filter-repo --replace-test <textfile>` 
    - Text file content - `github_secret>>>removed_github_secret`
    - This will chage git commit history, so force push is needed `git push origin main --force`
    - All other collab/developer must clone the repo again.
    - This will not change history of forks.

2. How do you undo your last commit without losing your changes?
    - We can use `git reset --soft HEAD^`
    - This will undo the last commit, keep the commit changes in stage area and also keep work area as is.
    - It has `--mixed` and `--hard` option
    - `--mixed` will bring all changes in work area.
    - `--hard` will clean the commit, stage and work area.

3. You need to discard local changes in a specific file. How would you do it?
    - Using `git restore <file-name>`
    - `git restore .` delete all changes in all file.
    - `git restore --staged <file-name>` to delete changes made in file in staged area.

4. What happens if you run git reset --hard HEAD~1?
    - This will delete last commit along with changes we had in stage and work area.

5. How can you recover a deleted branch?
    - Branch present in remote and deleted from local
        - `git pull origin <branch-name>`
    - Branch deleted from remote but present in local
        - ` git push origin <branch-name>`
    - Branch deleted from both places
        - We can `git reflog` to find the commit of that branch.
        - `git checkout -b <branch-name> <commit-id>`
        - Branch will created with that commit.

6. You accidentally committed changes to the wrong branch. How do you move them to the correct branch?
    - We can use `git cherry-pick` to achive this
    - Get the commit-id which need to move on branch using `git log --oneline`
    - checkout the required branch `git checkout <branch-name>` or `git switch <branch-name>`
    - Run `git cherry-pick <commit-id>`, commit moved to that branch

7. How do you revert a specific commit without affecting other changes?
    -  `git log --oneline` get commit id 
    - `git revert <commit-id>` will revert the commit.
    - Now commit the changes and push to update in remote.

8. You cloned a repository but forgot to specify --recurse-submodules. How do you initialize submodules afterward?
