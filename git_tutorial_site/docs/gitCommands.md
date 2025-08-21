## **1. Setup & Configuration**

```bash
git config --global user.name "Your Name"      # Set username
git config --global user.email "you@example.com"  # Set email
git config --global color.ui auto              # Enable colored output
git config --list                               # Show current config
```

---

## **2. Creating Repositories**

```bash
git init                                      # Initialize local repo
git clone <url>                               # Clone remote repo
```

---

## **3. Checking Status & History**

```bash
git status                                    # Show staged, unstaged, and untracked files
git log                                       # Show commit history
git log --oneline                             # Short commit history
git log --graph --all --decorate              # Visual commit graph
git diff                                      # Show unstaged changes
git diff --staged                             # Show staged changes
```

---

## **4. Staging & Committing**

```bash
git add <file>                                # Stage a file
git add .                                     # Stage all changes in current directory
git add -A                                    # Stage all changes including deletions
git commit -m "Commit message"               # Commit staged changes
git commit -am "Message"                      # Stage tracked files and commit
git reset <file>                              # Unstage a file
```

---

## **5. Branching**

```bash
git branch                                    # List local branches
git branch -r                                 # List remote branches
git branch -a                                 # List all branches
git branch <name>                             # Create new branch
git checkout <branch>                         # Switch branch
git checkout -b <branch>                      # Create + switch
git switch <branch>                           # Switch branch (newer syntax)
git switch -c <branch>                        # Create + switch (newer syntax)
```

---

## **6. Merging**

```bash
git merge <branch>                            # Merge branch into current
git merge --no-ff <branch>                    # Create merge commit even if fast-forward possible
git mergetool                                 # Launch tool to resolve conflicts
```

---

## **7. Cherry-Picking**

```bash
git cherry-pick <commit-hash>                 # Apply a specific commit to current branch
```

---

## **8. Rebasing**

```bash
git rebase <branch>                           # Reapply commits on top of another branch
git rebase --interactive <branch>            # Edit, squash, or reorder commits
git rebase --abort                            # Abort rebase if conflicts
git rebase --continue                         # Continue after resolving conflicts
```

---

## **9. Resetting & Reverting**

```bash
git reset --soft <commit>                     # Move HEAD, keep changes staged
git reset --mixed <commit>                    # Move HEAD, keep changes unstaged
git reset --hard <commit>                     # Move HEAD, discard changes
git revert <commit>                           # Create a commit that undoes a previous commit
```

---

## **10. Remote Repositories**

```bash
git remote -v                                 # Show remotes
git remote add <name> <url>                   # Add a remote
git remote remove <name>                      # Remove a remote
git remote rename <old> <new>                 # Rename a remote
git remote set-url <name> <url>              # Change remote URL

git fetch <remote>                            # Fetch changes from remote
git fetch --all                               # Fetch from all remotes
git pull <remote> <branch>                    # Fetch + merge
git push <remote> <branch>                    # Push local branch to remote
git push -u <remote> <branch>                # Push + set upstream
git push --all <remote>                       # Push all branches
git push --tags <remote>                      # Push tags
git push <remote> --delete <branch>          # Delete remote branch
git branch --set-upstream-to=<remote>/<branch>  # Link local branch to remote
```

---

## **11. Stashing**

```bash
git stash                                     # Save uncommitted changes
git stash list                                # Show stashes
git stash apply                               # Apply latest stash
git stash pop                                 # Apply and remove latest stash
git stash drop                                # Delete a stash
git stash clear                               # Remove all stashes
```

---

## **12. Undoing Changes**

```bash
git checkout -- <file>                        # Discard local changes in a file
git clean -f                                  # Remove untracked files
git reflog                                    # Show history of HEAD moves
```

---

## **13. Viewing Differences**

```bash
git diff                                      # Unstaged changes
git diff --staged                             # Staged changes
git diff <branch>                             # Differences from another branch
git show <commit>                             # Show commit details
```

---

## **14. Helpful Tips**

- `git log --oneline --graph --decorate --all` → visualize history.
- `git blame <file>` → see who last changed each line.
- `git shortlog` → summarize commits by author.

---
