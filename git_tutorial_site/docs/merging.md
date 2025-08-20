# Git Merge

`git merge` is used to combine changes from one branch into another.

## git merge

```bash
git merge <branch-name>
```

### Example

Suppose you are on `main` and want to merge a feature branch called `feature1`:

```bash
git checkout main      # Make sure you are on the branch you want to merge into
git merge feature1     # Merge changes from feature1 into main
```

- If there are no conflicts, Git will automatically merge the changes.
- If conflicts exist, Git will prompt you to resolve them manually.

---

- Git combines changes from both branches since they split from a common ancestor.

- Any new files in the branch being merged that aren’t in your current branch will be added.

- Any changes to existing files in the merged branch will be applied to your current branch.

- If both branches changed the same part of a file, Git will ask you to resolve a merge conflict.

---
