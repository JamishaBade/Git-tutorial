# Git Basics

## What is Git?

Git is a distributed version control system. It helps to track changes in files, typically source code. It allows to collaborate with group of people without overwriting eachother's work.

## Git Installation

### On macOS

Git comes bundled with the **Command Line Tools for Xcode**. To check if it’s installed, open Terminal and type:

```bash
git --version
```

or

```bash
git -v
```

## Setting Personal Info to Git

Git requires you to set your name and email before you start committing changes. This information is stored in your commits.

```bash
git config --global user.name "yourusername"
```

```bash
git config --global user.email "youremail@example.com"
```

## Basic Commands

follow along step by step:

1. Create a folder called `git_module`
2. Create a subfolder called `first_app`
3. Open your terminal and change directory `cd first_app`
4. `ls -l`: lists the files in the directory
5. `nano file1.txt`: creates a new file in the directory
6. In the text editor, write some texts
7. `Ctrl+X` and press Y

8. `git init`
   :This creates a hidden .git folder, which tracks changes in this project.

---

By this step, you have succesfully initialized a git repo

## Spoonfeed git changes

Git doesn’t automatically track changes in your files. You need to tell Git when a file is added, modified, or deleted.

Files that Git doesn’t know about are called untracked files.

Untracked files aren’t included in commits, and Git won’t keep a history of them until you explicitly add them.

If an untracked file is deleted before being added, Git cannot recover it.

Tip: Always use git status to see which files are untracked, modified, or staged for commit as they appear in red font colors.

## Adding git files

This is adding untracked files.

```bash
git add filename.txt
```

**_Here, the files are transformed from unstaging areas to staging area._**

If you have mutilple untracked files, then you can track it all at once.

```bash
git add .
```

## git status

To check the status of git:

```bash
git status
```

<span style="color:green">Files that Git already knows about. If changes are staged for commit, they appear in green..</span> </br>
<span style="color:red">New files Git doesn’t know about yet. These appear in red.</span>
