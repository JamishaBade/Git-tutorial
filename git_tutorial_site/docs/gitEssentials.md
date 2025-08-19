# git reset

Using `git reset ` you can:

- unstage files
- undo commits
- delete commits

The modes of `git reset` are:

- soft, mixed, hard

```bash
# bring the file to staging area
git reset --soft commitHash
```

```bash
# bring the file to unstaging area
git reset --mixed commitHash
```

! This is very risky command

```bash
# deletes the file
git reset --hard commitHash
```
