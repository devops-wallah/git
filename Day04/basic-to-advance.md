# Advanced Git Interview Questions (DevOps - 5 Years Experience)

## 1. Git Fundamentals (Advanced Understanding)

1. What is the difference between Git and other VCS tools like SVN?
2. Explain Git’s internal architecture.
3. What are Git objects? Explain blob, tree, commit, and tag objects.
4. How does Git store data internally?
5. What is the `.git` directory and what are its important components?
6. Explain the Git commit lifecycle.
7. What is the difference between `git fetch` and `git pull`?
8. What is the difference between `git merge` and `git rebase`?
9. When should you avoid using `git rebase`?
10. What is a fast-forward merge?

---

# 2. Git Branching & Strategies

11. What are different Git branching strategies used in DevOps?
12. Explain GitFlow workflow.
13. Explain Trunk-based development.
14. What is the difference between feature branch and release branch?
15. What happens internally when a branch is created?
16. How does Git identify the HEAD?
17. What is a detached HEAD state?
18. How do you recover from a detached HEAD state?
19. How do you delete local and remote branches?
20. How do you rename a branch locally and remotely?

---

# 3. Git Rebasing & History Management

21. What is interactive rebase?
22. How do you squash commits?
23. What is the difference between `git reset` and `git revert`?
24. Explain `git reset --soft`, `--mixed`, and `--hard`.
25. When should you use `git revert` instead of `git reset`?
26. How do you remove a commit from history?
27. What is `git cherry-pick`?
28. What is `git reflog` and how is it used?
29. How do you recover a deleted branch?
30. How do you recover lost commits?

---

# 4. Git Staging & Index

31. What is the Git staging area?
32. What is the difference between working directory, staging area, and repository?
33. How does `git add` work internally?
34. What is partial staging?
35. How do you stage only part of a file?

---

# 5. Git Conflict Management

36. What causes merge conflicts?
37. How do you resolve merge conflicts?
38. What is a rebase conflict and how do you resolve it?
39. How do you abort a merge or rebase?
40. What tools can be used for conflict resolution?

---

# 6. Git Performance & Large Repositories

41. How does Git handle large repositories?
42. What is Git shallow clone?
43. What is Git sparse checkout?
44. What is Git LFS (Large File Storage)?
45. When should Git LFS be used?

---

# 7. Git Hooks (DevOps Focus)

46. What are Git hooks?
47. What are common types of Git hooks?
48. What is the difference between client-side and server-side hooks?
49. Explain pre-commit hook use cases.
50. How can Git hooks be used in CI/CD pipelines?

---

# 8. Git Remote & Collaboration

51. What is a remote repository?
52. What is the difference between `origin` and `upstream`?
53. How does `git push` work internally?
54. What is force push?
55. What are the risks of `git push --force`?
56. What is `git push --force-with-lease`?
57. How do you track remote branches?
58. What is a pull request / merge request workflow?

---

# 9. Git Security

59. How do you sign commits in Git?
60. What is GPG signing?
61. How do you remove sensitive data from Git history?
62. What tools can be used to clean Git history?
63. How do you prevent secrets from being committed?

---

# 10. Git Troubleshooting

64. How do you fix a broken commit history?
65. What happens if you accidentally commit to the wrong branch?
66. How do you undo the last commit without losing changes?
67. How do you undo a pushed commit?
68. How do you resolve "non-fast-forward" push errors?
69. What is `git bisect` and how is it used?

---

# 11. Git Internals (Very Advanced)

70. How does Git calculate commit hashes?
71. What is the Git DAG (Directed Acyclic Graph)?
72. How does Git garbage collection work?
73. What is `git gc`?
74. What are packfiles?
75. What is the difference between loose objects and packed objects?

---

# 12. DevOps Scenario Based Questions

76. How would you manage Git in a microservices architecture?
77. How do you handle hotfixes in production using Git?
78. How would you enforce branch protection in Git?
79. How would you manage Git access control in an enterprise environment?
80. What Git practices improve CI/CD pipeline efficiency?

---

# 13. Real World Scenarios

81. A developer force pushed and broke history. How do you recover?
82. A secret key was committed to Git. What steps do you take?
83. Your repository size suddenly increased drastically. How do you debug?
84. CI pipeline fails after merge. How do you troubleshoot?
85. Multiple developers are committing directly to main branch. How do you fix the workflow?
