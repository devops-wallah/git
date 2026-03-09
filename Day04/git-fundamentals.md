# Git Fundamentals (Advanced Understanding)

1. What is the difference between Git and other VCS tools like SVN?
    - Git is Distributed VCS
    - No separate copy created form branch or commit
    - lightweight

2. Explain Git’s internal architecture.
    - when we `git init` it create .git folder
    - which has `HEAD, config, description, index, refs, hooks, logs, info and objects`
    - `HEAD` store the current branch `ref: refs/heads/day-4` or commit hash
    - `config` store the repo specific config like `name, email, remote`
    - index store the all details about staged files in encoded format.

3. What are Git objects? Explain blob, tree, commit, and tag objects.
    - Blob = file content
    - Tree = folder structure
    - Commit = snapshot + history
    - Hash = identity + integrity

4. How does Git store data internally?
    - In object mentioned above

5. What is the `.git` directory and what are its important components?
    - `HEAD, config, description, index, refs, hooks, logs, info and objects`

6. Explain the Git commit lifecycle.
    - working area > git add > create blob object for added file > git commit > update blob and create commit hash

7. What is the difference between `git fetch` and `git pull`?
    - Fetch will bring all remote branches to local as origin/branch-name
    - Pull fetch all remote branches but merge only current HEAD branch

8. What is the difference between `git merge` and `git rebase`?
    - Merge will create new extra commit which rebase just update the branch with updated commit hash.

9. When should you avoid using `git rebase`?
    - Rebase is safe for local/private branches but dangerous for shared/public branches. Merges preserve history and avoid conflicts for teammates.

10. What is a fast-forward merge?
    - If we create branch from main and worked on it, but main is still as is and not new commit added then when we try to merged our branch it will do FF merge. This will not create merge commit.