## GIT


### Flushing local changes
```
git reset --hard origin/develop
```

```
git reset –hard
git clean -fxd
```



### Rebasing

```
git rebase --onto newBase oldBase feature/branch
```

#### interactive rebase
```
git rebase -i HEAD~3
```

### Logging
```
git log --oneline
```
