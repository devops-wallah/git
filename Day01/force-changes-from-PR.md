# How we can enforce the developers to make any changes via PR only and have approval from at least 2 reviewer?

### We can configure the branch protection rule to force developers to not directly merge on main branch and changes must come from PR

**Branch protection and Ruleset works alongside to apply rule.**

- Require a pull request before merging
- The number of approving reviews that are required before a pull request can be merged.
- Require an approving review in pull requests that modify files that have a designated code owner.
- All conversations on code must be resolved before a pull request can be merged.
- When merging pull requests, you can allow any combination of merge commits, squashing, or rebasing. At least one option must be enabled.
- Block force pushes - Prevent users with push access from force pushing to refs.

- Require status checks to pass - Choose which status checks must pass before the ref is updated. When enabled, commits must first be pushed to another ref where the checks pass.

- Require code quality results - Choose which severity levels of code quality results should block pull request merges. When configured, a code quality analysis must be done on the pull request before the changes can be merged.