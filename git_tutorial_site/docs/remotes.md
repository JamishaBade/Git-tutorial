# Remote Repository

## Intro

A remote is simply a Git repository that lives on another machine, serving as a designated common ancestor for a distributed team. It is the bridge that connects your local, isolated development history to the shared project timeline.
<br>
**_It is a new synchronized paradigmn._**

It allows you to share and collaborate with other developers by providing a central, common reference point (the remote repository) to synchronize your work.

```bash
git remote add origin url
```

```bash
#Use to check which remotes are already connected
git remote -v
```

```bash
git remote rename <old> <new>
```

```bash
#remove a remote
git remote remove <name>
```

```bash
git branch -r
```

```bash
# Syntax: git push <remote-name> <branch-name>
git push origin main
```

```bash
git push -u origin main
# After this, you can just use:
git push
git pull
```

## Cloning

git clone is the command to create a complete, new local copy of an entire remote repository.

```bash
# Syntax: git clone <repository-url>
git clone https://github.com/user/project-name.git
```

## Fetching

```bash
git fetch <remote> # Download changes from remote (doesn’t merge).

git fetch --all # Fetch from all remotes.
```

## Pulling

It is essentially the combination of fetch and merge

```bash

git pull <remote> <branch> # Fetch + merge changes from remote into current branch.

git pull --rebase # Fetch + reapply your changes on top (avoids merge commits).
```

## Pushing

```bash
git push <remote> <branch> # Push local branch to remote.

git push -u <remote> <branch> → Push and set upstream (so you can just git push next time).

git push --all → Push all branches.

git push --tags → Push all tags.

git push <remote> --delete <branch> → Delete a branch from remote.
```

## Tracking & Upstream

```bash
git branch -r → Show remote-tracking branches.

git branch -a → Show all branches (local + remote).

git branch --set-upstream-to=<remote>/<branch> → Link local branch to remote branch.

git fetch -p → Prune (remove deleted remote branches from local references).
```
