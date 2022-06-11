Need to update

## Version
- 

## .bash_profile
- This file is run when login shell logins as bash.
- Set environment variables in this file.
- Environment variables are taken over to other bash processes.
- Write read `.bashrc` file at last.

```
// read .bashrc file at last.
test -r ~/.bashrc && . ~/.bashrc
```

## .bashrc
- `rc` means `run command`.
- This file is run when start new bash.
- Define aliases and shell script in this file.
- Set variables which is not environment variables.

## Reference
- [.bashrc と .bash_profileの使ひ分け](https://qiita.com/magicant/items/d3bb7ea1192e63fba850)
- [Bash: .bashrcと.bash_profileの違いを今度こそ理解する](https://techracho.bpsinc.jp/hachi8833/2021_07_08/66396)
- [.bash_profileとは｜「分かりそう」で「分からない」](https://wa3.i-3-i.info/word13650.html)
