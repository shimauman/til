## Version
- 

## Commands
### Check
```
$ git stash list
```

### Add
```
$ git stash
```
```
// -u is --include-untracked. Includes unadded changes.
$ git stash -u
```
```
$ git stash save message
```

### Apply
```
// Added changes -> unadded changes
$ git stash apply stash@{index}
```
```
// Added changes -> added changes
$ git stash apply stash@{index} --index
```
```
$ git stash pop stash@{index}
```

### Remove
```
$ git stash drop stash@{index}
```
```
$ git stash clear
```

## Reference
- 
