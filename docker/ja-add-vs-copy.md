## Version
- 

## ADD
ローカルにある圧縮されたファイルをコンテナへ複製したい時に。自動で解凍をしてくれる。
ADDのベストな使い方は、ローカルの`tar`ファイルをイメージに自動展開する用途。
```dockerfile
ADD {path to compressed source in local} {path to destination in container}
```
## COPY
ファイルをコンテナへ複製したい時に。ADDより意図・機能が明確なため、COPYの方が望ましい。
```dockerfile
COPY {path to source in local} {path to destination in container}
```

## Reference
- [Docker docs ja: ADDとCOPY](https://docs.docker.jp/engine/userguide/eng-image/dockerfile_best-practice.html#add-copy)
