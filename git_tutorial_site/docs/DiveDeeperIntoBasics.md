# Git Dive Deep

## git init

- default branch created while using git init is the master branch.
- When we initialize the repo, two regions are created.
- **Staging area** (where changes are prepared before commit)
- **Non-staging area** (working directory with untracked/modified files)

The `.git` directory contains:

- HEAD file (references current branch)
- config file (repository configuration)
- objects directory (stores all content)
- refs directory (stores pointers to commits)

### Remove a local git repo

```bash
rm -rf .git/
```

This deletes the repository history.

### Rename default branch name

```bash
git init --initial-branch=main
```

Sets initial branch to main instead of master.

Nested git repository.
Never create a git repo inside a repo.
Avoid this to avoid chaos.

Never create a git repo inside another repo (except for submodules)

Potential issues:

- Conflicting .git directories

- Confusing version control boundaries

- Complex merge behaviors

---

## git add

### Core Functionality

Stages changes from working directory to staging area

### Advanced Usage

```bash
# Interactive add (choose hunks)
git add -p

# Add all tracked files (not new files)
git add -u

# Add by file pattern
git add '*.js'
```

### Behind the Scenes

- Creates SHA-1 hashes of file contents
- Stores compressed versions in object database
- Updates index file with new file modes and hashes

---

## git commit

### Commit Anatomy

Creates a commit object containing:

- Author info
- Commit message
- Pointer to tree object (snapshot of repo)
- Pointer to parent commit(s)

### Advanced Options

```bash
# Amend previous commit
git commit --amend

# Sign commit cryptographically
git commit -S

# Commit with multiline message
git commit -m "Title" -m "Description"
```

### Technical Details

- Each commit has a unique SHA-1 hash
- Commit objects reference tree objects
- Tree objects reference blob objects (files) and other trees

---

## git push
