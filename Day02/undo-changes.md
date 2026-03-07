## Scenario -

# How you can undo the last commit without lossing the changes you already made?

** We can use `reset` cmd to achive this

- `git reset` comes with 3 options
    - `--soft` This will keep changes from commit, staging and working area.
    - `--mixed` default option. This will keep changes from commit and stagin area only.
    - `--hard` This will remove changes from all place.
    
- If you do hard reset to last 4th commit and want to get back your previous commit changes.
    - Use ` git reflog` to get commit has where you want to go
    - `git reset --hard <commit id>` your HEAD will be at that commit and changes will be in place.
