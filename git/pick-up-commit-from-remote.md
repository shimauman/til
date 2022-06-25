## Version
- 

## How To
We can pick up specific commit from remote and apply it to local.
```
$ git cherry-pick commit-id
```

### Use Case
When we review `sample/branch`,
```
$ git fetch --prune
$ git checkout sample/branch
```

↓

Pick up new added commit(12345a) from remote `sample/branch` and apply it to local `sample/branch`.
```
$ git cherry-pick 12345a
```

## Reference
- 
