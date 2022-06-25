## Version
- 

## Issue
git bashで
- `/{path to mounted source}`の先頭にgit bashのルートディレクトリのpathが追加される。
- `;C`フォルダがsource側に作成される。
- `/{path to mounted source};C`と解釈される。

## Solution
Format
```
docker run -it --rm -u -v /$PWD/{path to mounted source}:/{path to target directory} {image id} bash
```
Sample
```
docker run -it --rm -v /$PWD/source:/root/target 6a7b7ca24774 bash
```
## Reference
- 
