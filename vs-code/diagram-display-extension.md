## Version
- 

## Markdown Preview Mermaid Support Extension
1. Install the extension.
2. Make markdown file.
3. Write code block with mermaid syntax.

## Sample
This is sample code from the below reference.
```mermaid
sequenceDiagram
    actor クライアント
    participant API as API Gateway<br/>Rest API
    participant Lambda as Data Post<br/>Lambda Function
    participant DataTable as Amazon DynamoDB<br/>Data Table
    participant SES as Amazon SES

    クライアント ->>+ API: データ登録
    API ->>+ Lambda: データ登録
    Lambda ->> Lambda: バリデーション
    alt バリデーションエラーの場合
      Lambda -->> API: バリデーションエラー
      API -->> クライアント: 400 BadRequest
    end
    Lambda ->>+ DataTable: データ登録
    DataTable -->>- Lambda: 登録OK
    Lambda ->>+ SES: メール送信依頼
    SES -->> Lambda: 送信受付OK
    SES ->>- クライアント: 登録確認メール送信
    Lambda -->>- API: 登録OK
    API -->>- クライアント: 200 OK
```

## Reference
- [mermaid-js docs : Diagram Syntax](https://mermaid-js.github.io/mermaid/#/n00b-syntaxReference)
- [Developers IO : よくあるAWSサーバーレス構成のシーケンス図をMarkdown（Mermaid）で描いてみた](https://dev.classmethod.jp/articles/drawing-a-sequence-diagram-of-a-common-aws-serverless-configuration-with-mermaid/)
