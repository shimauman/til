TODO: Need to update.

## Version
- 

## API
情報や機能が外部から利用できるようにする仕組み。
Web APIは、Webを介して利用するAPIを指す。

## RESTful API (REST API)
RESTに従って設計されたAPIのこと。

## REST
RESTとは、REpresentational State Transferの略。
複数のソフトウェアを連携させる際に適した設計の指針。

### 1. アドレス可能性 - Addressability
提供する情報がURIを通して、表現できている。
全ての情報は、一意なURIで表現されるアドレスを持つ。

### 2. ステートレス性 - Stateless
HTTPをベースに、ステートレスである。
セッション管理などはしない。

### 3. 接続性 - Connectability
情報の内部に、別の情報などへのリンクを含めることができる。

### 4. 統一インターフェース - Uniform Interface
情報への操作(取得、作成、更新、削除)は全てHTTPメソッド(GET / POST / PUT / DELETE)を利用する。

## Reference
- [IBM documentation : RESTful API の設計](https://www.ibm.com/docs/ja/zos-connect/zosconnect/3.0?topic=apis-designing-restful)
- [Qiita : リソース指向アーキテクチャ(ROA)とは何なのか](https://qiita.com/NagaokaKenichi/items/0f3a55e422d5cc9f1b9c)
- [Hatena : REST APIとは？ざっくりと理解してみる](https://tech.012grp.co.jp/entry/rest_api_basics)
