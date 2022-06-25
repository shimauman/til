## Version
- 

## Compress Docker Image To `tar` File
docker imageをtarファイルに圧縮、解凍。
```
$ docker save {image} > {tar file}
```

## Uncompress the `tar` File
```
$ docker load < {tar file}
```

## Use Case
docker imageを置くサーバーが、セキュリティの観点などからインターネットに接続できない際に、
 - docker imageをtarファイルに圧縮してサーバーに送る。
 - サーバー内で圧縮ファイルを解凍する。
 - サーバー内で解凍したdocker imageをrunする。

docker hubなどのdocker resistoryは、インターネットを経由してdocker imageを取得するため、今回のケースでは利用することができない。

## Reference
- 