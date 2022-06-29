## Version
- 

## Command
```
ls -la
```
- `a` : all
- `l` : long, show details

## Result
```
$ ls -la

drwxr-xr-x 1 taro 111111    0  3月  9 16:47 .
drwxr-xr-x 1 taro 111111    0  3月  8 15:21 ..
drwxr-xr-x 1 taro 111111    0  3月 11 20:15 .git
-rw-r--r-- 1 taro 111111  756  2月 26 18:12 annotation-comments.md
drwxr-xr-x 1 taro 111111    0  3月  5 11:12 aws
drwxr-xr-x 1 taro 111111    0  1月 30 14:17 cypress
drwxr-xr-x 1 taro 111111    0  3月  8 11:55 docker
```

## Detail Of The Result
```
d / rwxr-xr-x / 1 / taro / 111111 / 0 / 3月  8 11:55 / docker

file-type / permission / counts-of-hardlink / owner-name / group-name / bite-size / time-stamp / file-name-or-directory-name-or-symbolic-link-name
```

### File Type
- `-` : file
- `d` : directory
- `l` : symbolic link

### Permission
- `r` : Read
- `w` : Write
- `x` : Execute

### Partition
```
rwxr-xr-x
rwx / r-x / r-x
Owner / Group userグループユーザのアクセス権限 / その他ユーザのアクセス権限
```

### Example Of Symbolic Name
```
fileA-symbolic -> fileA
```

## Reference
- 
