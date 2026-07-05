# Git

## Overview
Git is essential for collaboration and release management. In interviews, it is important to explain how branches, merges, conflict resolution, and pull requests work in practice.

## Key Concepts
- Repository, commit, branch, merge, rebase
- Pull requests and code reviews
- Conflicts and resolution
- Cherry-pick and stash

## Frequently Asked Interview Questions (moved to spring-questions.md)

## Detailed Answers
### 1) Merge vs rebase
`git merge` keeps history and integrates branches. `git rebase` rewrites commit history to create a cleaner line of development, but requires caution when sharing branches.

### 2) Pull request
A pull request is a review mechanism where one team member proposes changes and others review them before merging.

### 3) Merge conflicts
Merge conflicts happen when two branches change the same lines. The resolution requires manually choosing the correct final content.

### 4) `git stash`
`git stash` temporarily stores changes so you can work on something else without losing progress.

### 5) Commit history
A clean commit history helps with debugging, release planning, and understanding why a change was made.

### 6) Fetch vs pull
`git fetch` downloads remote updates without merging them. `git pull` fetches and immediately merges.

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
