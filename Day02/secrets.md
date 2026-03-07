## Scenario -
# You accidentaly pushed secrets on remote. How to remove it from git history?

## We can use `git filter-repo` to do it. If we use `revert` it will still present in history. 

Here is how we can use it - 

`git filter-repo` doesn't come up with git. You can install using `pip install git-filter-repo`

Note - Please always clone a fresh repo to performe below actions.

- To remove the secret text from repo
    - Create text file `replace.txt` with `Secret_Value>>>Replaced_Value`
    - Now run `git filter-repo --replace-text replace.txt`
    - It will remove the Secret from entire git history.

- To Remove entire file from history
    - Run ` git filter-repo --path "exact/path/to/file" --invert-paths`
    - This will remove file from enire history

This has chaged our git history, so we have to update remote with this changes. 
Run `git push origin main --force --all`

Now remote will not have any secret or file.

All collaborator need to clone the fresh repo cause the history has changed.
