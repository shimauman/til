## Case Sensitive
- 大文字小文字を区別
- ⇔ case insensitive

## Whitespaces
- leading whitespaces : 先頭の空白
- trailing whitespaces : 末尾の（末尾に後続している）空白
- duplicate whitespaces

## Context
利用者の意図や状況、環境などの総体を表したり、同じ処理や記述でも状況に応じて動作などが異なる場合に、その選択基準となる判断材料や条件などを指す場合が多い。

例えば、
`$item`が何であっても処理は変わらない。ここでいう`$item`が`context`みたいなもの。
```php
function shopping(string $item): void
{
    addCart($item);
    pos($item);
    payment($item);
    intoBag($item);
}
```

## State
例えば、
`$item`によって処理が変わる。ここでいう`$item`が`state`みたいなもの。
```php
function shopping($item: string){
    if ($item === 'banana') {
        ***
    }
    if ($item === 'apple') {
        ***
    }
}

```

### Reference
- [Qiita : context?state?](https://qiita.com/dojyorin/items/0bd3ef167991cfc703b1)

## REPL
Read Eval Print Loop。対話型実行環境。ターミナルでの実行環境みたいな感じ。
- Read : キーボードから打ち込まれた命令を読み込む。
- Eval : 評価・実行。
- Print : 結果を表示する。
- Loop : それを繰り返す。

## Stack Trace
エラーが表示された時に、そのエラーに至るまでどのような処理がなされたのかを、表示させたもの。

## Workaround
応急処置のこと。根本的な解決はあとで。

## デグレ―ション
degradation、劣化。前よりおかしくなっちゃった、前の方が良かったな状態。

## リグレッション
regression、回帰。regression testとは、デグレってない？を確認するために行うテスト。

## rc
release candidate。正式にリリースされる前のバージョン。ベータ版よりもリリースに近い。
```
1.0.0-rc3
```

## Blue/Greenデプロイ
現在稼働している環境(Blue)とは別に本稼働予定環境(Green)を用意し、ロードバランサーなどでルーティングを新しい環境にパッと向ける。

### Reference
- [Qiita : AWS CodeDeploy でEC2のBlue/Greenデプロイを作成する](https://qiita.com/keitakn/items/6abe6c971e4dec3b69ef)<br>
- [Google Cloud : アプリケーションのデプロイとテストの戦略](https://cloud.google.com/solutions/application-deployment-and-testing-strategies?hl=ja#bluegreen_deployment_pattern)

## Canary Release
現在稼働している環境(Blue)とは別に本稼働予定環境(Green)を用意し、ロードバランサーなどで、一部のユーザーだけを新バージョンにアクセスさせる。徐々に稼働環境を切り替える。Google Cloudの記事では、Rolling Updateと表現されていた。

### Reference
- [日経TECH : カナリアリリース](https://xtech.nikkei.com/atcl/nxt/keyword/18/00002/081900087/)
- [Google Cloud : アプリケーションのデプロイとテストの戦略](https://cloud.google.com/solutions/application-deployment-and-testing-strategies?hl=ja#rolling_update_deployment_pattern)

## Declarative programming / 宣言的プログラミング
- 何をやりたいかを書くプログラム方法。SQLなどが該当する。このデータがほしいというように目的を一文で書くSQL。
- ⇔ Imperative: 命令的・指示的。

### Reference
- [Qiita : 宣言的？ Declarative?](https://qiita.com/Hiroyuki_OSAKI/items/f3f88ae535550e95389d)

## ディレクティブ
- directive : 指令
- プログラムを機械語に変換する際に、変換プログラム(コンパイラなど)に渡す指示や情報のこと。

## リテラル
- literal : 文字の、文字通りの、文の一語一語を忠実にたどる様(逐語的な)。
- コードの中に直接べた書きした文字や数字。

```php
// '田中'や20がリテラル
$name = '田中';
$age = 20;
```

## 構成ドリフト
例えば、aws cdkでstackをコード管理している。そのコードに記された状態と実際のインフラの状態が違う。このような状況を構成ドリフトという。AWSコンソールから操作もできるようになっているなど、自動と手動が混在している時に起こり得る。

## ポーリング
- poling
- 一定間隔で問い合わせること。例えば、たまっているjobは無いか？など問い合わせたり。

## Queue / Job / Worker
```
メール送信ボタンをpush
↓
↓裏では(非同期処理)、メール送信の処理が動いている。
↓
送信完了と表示
```

### Queue
実行されるのを待つJobのリスト。

### Job
処理内容。メールを送信すること。

### Worker
Jobを処理するプロセス。実際にメール送信を実行する。

## Zero Padding
指定した桁数に満たない部分を`0`で埋めること。
```
1 -> 01
```

## O/Rマッピング
Object/Relationマッピングのことで、オブジェクトとリレーショナルデータベースをマッピングすること。

ORMにより、DBからデータを取得、取得したデータをオブジェクト化、DBに格納 をSQL自体を書かずに実装できる。

メリットとして、テーブルなどに変更があっても、SQL文の書き換えを行う必要がない。

### Reference
- [Qiita : もっとORMを使えるようになりたいので、見直してみた](https://qiita.com/niisan-tokyo/items/156eb35c6eeaf07b9b65)