# Git Basic

> Created by Fisher at 23:08 on 2017-04-13.


## [Undo Last Commit](http://stackoverflow.com/questions/927358/how-to-undo-last-commits-in-git)

```bash
git reset HEAD~
```


## [Git Undo `git reset HEAD~`](http://stackoverflow.com/questions/2510276/undoing-git-reset)

```bash
git reset 'HEAD@{1}'
```

## [Undo All Working Dir Changes Including New Files](http://stackoverflow.com/questions/1090309/git-undo-all-working-dir-changes-including-new-files)

```bash
git reset --hard # removes staged and working directory changes
git clean -f -d # remove untracked

## !! be very careful with these !!
## you may end up deleting what you don't want to
## read comments and manual.
git clean -f -d # remove untracked
git clean -f -x -d # CAUTION: as above but removes ignored files like config.
git clean -fxd :/ # CAUTION: as above, but cleans untracked and ignored files through the entire repo (without :/, the operation affects only the current directory)
```

## Assume Local Files Unchanged

Assume changed files unchanged.

```bash
git update-index --skip-worktree [<file>...]
```

- StackOverflow: [Ignore files only locally in git](https://stackoverflow.com/questions/1753070/how-to-ignore-files-only-locally-in-git).
- StackOverflow: [Difference Between `assume-unchanged` and `skip-worktree`](https://stackoverflow.com/questions/13630849/git-difference-between-assume-unchanged-and-skip-worktree/13631525#13631525).

## Branch

### Create a new branch and checkout to it.

```bash
git checkout -b <branch-name>
```

## Tag

```bash
# Show local tags.
git tag

# Create a tag.
git tag -a v0.1 -m 'version v0.1'

# Tag specific commit.
git tag -a v1.2 9fceb02

# Push tag to remote.
git push <remote-name> <tag-name>
git push origin v0.0.1
```
