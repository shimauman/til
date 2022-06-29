## Version
- 

## Change Aceess Mode
Change access permissions for the file and directory.

## Sample 1
```
$ chmod 744 file-path
$ chmod 744 -R directory-path
```

```
Owner / Group users / Other users
7 / 4 / 4
```

### Terms
- Owner : Who has the files and folders.
- Group users : Who belong to same group with the Owner.

### Permission Numbers
- `4` : Read
- `2` : Write
- `1` : Execute
- `0` : No permission
- `7` : 4+2+1, all permission

## Sample 2
```
chmod a+w file-path
chmod -R a+w directory-path
chmod -R a+w directory-path directory-path
```

### Permission Labels
- `r` : Read
- `w` : Write
- `x` : Execute

### Targets
- `u` : Owner permission
- `g` : Group users permission
- `o` : Other users permission
- `a` : All targets

### Operations
- `+` : Add following permission
- `-` : Remove following permission
- `=` : Change to following permission

### Examples
- `a+w` : Add writing permission on all targets.
- `o-r` : Remove reading permission from other users.

## Reference
- 