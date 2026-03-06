# Is it possible to push to remote branch without cloning the repo?

- ## Yes, it is possible to push the code to remote branched without cloning the repo. To achive this we need to create empty dir and initialize git there. after that we add remote and pull required branch. Then make changes and push it.

- ## Another approch we can follow is using Github API's using tokens.

## Steps

- `mkidr my-repo && cd my-repo`
- `git init`
- `git remote add origin <ssh/https URL>`
- `git pull origin <branch-name>`

## Now make changes to code 

- `git add .`
- `git commit -m "pushed without cloning repo"`
- `git push origin <branch-name>`
