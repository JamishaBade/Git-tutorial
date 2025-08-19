# Git Dive Deep

## git init

- default branch created while using git init is the master branch.
- When we initialize the repo, two regions are created.
- **Staging area** (where changes are prepared before commit)
- **Non-staging area** (working directory with untracked/modified files)

### remove a local git repo

```bash
rm -rf .git/
```

rename default branch name

```bash
git init --initial-branch=main
```

Sets initial branch to main instead of master.

Nested git repository.
Never create a git repo inside a repo.
Avoid this to avoid chaos.

---

## git add

---

## git commit
