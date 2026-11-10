# Git Workflow Documentation

## 1. Repository Setup

The project repository was created on GitHub and cloned to the local machine.

```bash
git clone <repository-url>
cd Elevate-Labs-DevOps-Task-4
```

## 2. Initial Commit

Project files were staged and committed.

```bash
git add .
git commit -m "Initial commit: Set up DevOps Git project structure"
git push -u origin main
```

## 3. Branch Creation

Three types of branches were used.

```bash
git checkout -b dev
git push -u origin dev
```

Feature branches were created for individual changes.

```bash
git checkout -b feature/add-project-info
```

## 4. Feature Development

Changes were committed and pushed to the feature branch.

```bash
git add .
git commit -m "Add project information feature"
git push -u origin feature/add-project-info
```

## 5. Pull Request and Merge

A Pull Request was created on GitHub to merge the feature branch into dev.

The Pull Request was reviewed and merged.

## 6. Merge Conflict Resolution

A merge conflict was intentionally created by modifying the same line in two different branches.

Git reported a content conflict in `src/app.py`.

The conflict was resolved manually, followed by:

```bash
git add src/app.py
git commit -m "Resolve merge conflict between dev and feature branches"
git push origin dev
```

## 7. Branch Cleanup

Merged feature branches were deleted.

```bash
git branch -d feature/update-message
git branch -d feature/conflict-demo

git push origin --delete feature/update-message
git push origin --delete feature/conflict-demo
git push origin --delete feature/add-project-info

git fetch --prune
```

## 8. Git Tagging

A version tag was created and pushed.

```bash
git tag -a v1.0.0 -m "Task 4 initial release"
git push origin v1.0.0
```

## 9. Verification

The following commands were used to verify the repository.

```bash
git status
git branch -a
git log --oneline --graph --all
git tag
```

## Conclusion

The project demonstrates Git version control, branching, commits, Pull Requests, merge conflict resolution, branch cleanup and version tagging.