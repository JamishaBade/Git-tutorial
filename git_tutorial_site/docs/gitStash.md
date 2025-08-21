# **Git Stash: Essential Commands**

git stash is a command that temporarily shelves (saves) the changes you're currently working on. It lets you quickly clean up your workspace without having to make a permanent commit, so you can switch to another task. When you're ready, you can "unpause" and get your changes back exactly as you left them.

#### **Save Work**

```bash
git stash                      # Shelve all current changes
git stash -m "message"         # Shelve with a description
```

#### **View & Restore**

```bash
git stash list                 # Show all shelved items
git stash pop                  # Restore latest & remove from shelf
git stash apply                # Restore latest but keep on shelf
```

#### **Clean Up**

```bash
git stash drop                 # Discard latest shelved item
git stash clear                # Empty entire shelf
```

#### **Advanced**

```bash
git stash --keep-index         # Shelve but keep staged files
git stash --include-untracked  # Shelve including new files
```
