TODO: Need to update.

## Version
- Semantic Versioning v2.0.0

## What
- The rule proposal to solve dependency hell.

## Version Number
```
v 1.2.3
```
```
1: Major Version
Increments this when we make incompatible API changes.
```
```
2: Minor Version
Increments this when we add functionality in a backwards compatible manner.
```
```
3: Patch Version
Increments this when we make backwards compatible bug fixes.
```

## Note
Q. パブリックなAPIを宣言すると、公式ドキュメントにあった。他のパッケージなどからAPIで利用される場合は、このバージョン管理を行うことで、APIを利用する側から見てこのパッケージは依存性の観点から扱いやすくなる。もし、他のパッケージなどからAPIで利用されない場合の、このバージョン管理を行う意味とは？そのパッケージの開発者達にとって、自分たちのバージョンがいくつでどんな種類の変更があったのかを共有する？
 
A. もし、外部から使われないようなAPIを持っていないのであれば、やる必要はない。しかし、特定コミットへversionなどのタグを付ける意味はある。例えば、本番環境でバージョンタグ`0.0.4`が付いたコミットまで正常に動いていたが、バージョンタグ`0.0.5`が付いたコミットまでが反映されたときにバグが確認されたら、`0.0.4`と`0.0.5`間のコミットの中にバグがあったと推測できる。


## Reference
- [Semantic Versioning official? docs](https://semver.org/)
