# Git

## Overview
Git is the standard version control tool used to track code changes, coordinate collaboration, and manage release workflows.

## Key Concepts
- Repository, commit, branch, merge, rebase
- Pull requests and code reviews
- Conflicts and resolution
- Cherry-pick and stash

## Frequently Asked Interview Questions
1. What is the difference between `git merge` and `git rebase`?
2. What is a pull request?
3. How do you resolve merge conflicts?
4. What is `git stash` used for?

## Answers
`git merge` preserves history while integrating branches, while `git rebase` rewrites commit history for a cleaner linear flow. A pull request is a review process for proposed changes. Merge conflicts occur when different changes touch the same lines. `git stash` temporarily saves uncommitted work.

## Code Examples
```bash
git checkout -b feature/login
git add .
git commit -m "Add login flow"
```

## Best Practices
- Commit small and descriptive changes.
- Review diffs carefully before merging.
- Keep branches focused and short-lived.

## Common Mistakes
- Committing unrelated files together.
- Forgetting to pull latest changes.
- Not resolving conflicts promptly.

## Real-World Scenarios
A team may use branches and pull requests to manage feature development, bug fixes, and release readiness.
