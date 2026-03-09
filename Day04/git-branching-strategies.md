# Git Branching & Strategies

1. What are different Git branching strategies used in DevOps?
    - Gitflow   
    - Trunk Based
    - GithubFlow

2. Explain GitFlow workflow.
    - One main branch and develop branch
    - other release, feature, hotfix short lived

3. Explain Trunk-based development.
    - One main branch and other short lived (<1 day>)

4. What is the difference between feature branch and release branch?
    - Feature branch used to bring new feture
    - release branch used to deploy the tested feature to prod

5. What happens internally when a branch is created?
    - The HEAD is pointing to same last commit from previous branch but via ref this branch
    - HEAD will be refs/head/new-branch-name/last-commit

6. How does Git identify the HEAD?
    - Using the file `.git/HEAD`

7. What is a detached HEAD state?
    -HEAD is pointing to specific commit

8. How do you recover from a detached HEAD state?
    - By checking out to the branch

9. How do you delete local and remote branches?
    - local using `git branch -D branc-name`
    - Remote - `git push --delete origin branch-name`

10. How do you rename a branch locally and remotely?
    - Local - `git branch -m old-name new-name`
    - Remote - don't have direct cmd, but we can push ne branch by chnaging name at local and then delete remote branch.