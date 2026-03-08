# Remote Repository & Collaboration Scenarios

1. Your team is working on the same file, and a colleague has already pushed changes. How do you avoid overwriting their work?
    - Pull the changes. Rebase my branch. Resolve conflict if any.
    - Commit and push.

2. You made some local commits but need to push them to a remote branch with a different name. How do you do that?
    - If want change only last commit msg then its easy.
        - Use ` git commit --amend -m "new msg"`
    - If commit is old.
        - Use `git rebase -i <commit-id>`. Note. Commit id must be previous of the commit you want to update msg.
        - e.g if you want 3rd commit msg then pass commit id if 4th commit
        - Change `pick` to `reword` in terminal for the commit id. Save using `esc + :wq!`
        - Enter new commit msg and save.
        - This will change the commit history. Use wisely.
    
3. How do you force push a commit while ensuring you don't overwrite other team members' work?
    - We can use `git push --force-with-lease` 
    - This will return error if remote has the changes which are not present on our branch.
    - Safe way is alway rebase our branch with main.

4. A team member deleted a remote branch. How can you recover it if you still have it locally?

5. You need to contribute to an open-source project. What steps will you take to fork and create a pull request?

6. How do you revert a pushed commit that is causing issues in production?
