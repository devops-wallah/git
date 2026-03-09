# Git Staging & Index

1. What is the Git staging area?
    - keep the changes to be commited

2. What is the difference between working directory, staging area, and repository?
    - Work area - we edit files
    - Stage area - put work completed file
    - repo - store changes in local repo

3. How does `git add` work internally?
    - git add > new blob object created for changes file 
    - object hash and other details like auther, files , size all store in index file

4. What is partial staging?
    - when we want to stage only some part of our worked file.
    - we use `--patch` option to stage it

5. How do you stage only part of a file?
    - git add -p file.txt

---

#  Git Conflict Management

6. What causes merge conflicts?
7. How do you resolve merge conflicts?
8. What is a rebase conflict and how do you resolve it?
9. How do you abort a merge or rebase?
10. What tools can be used for conflict resolution?
