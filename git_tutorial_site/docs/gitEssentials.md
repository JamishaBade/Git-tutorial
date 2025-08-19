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

```bash
# deletes the file. DANGEROUSS
git reset --hard commitHash
```

# git revert

```bash
git revert commitHash
```

### Soo, what is the difference between `git revert` and `git reset --hard`

- `git revert`- undos safely, creates a new commit
  you can recheck the old content using
  `git checkout hash`

---

- `git reset --hard` - deletes history, dangerous
  you cannot recheck teh old content ones deleted `:(`
