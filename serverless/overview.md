## Version
- Serverless Framework v3
- Serverless requires Node.js v12 or more

## OverView
Serverless Framework is
- the tool to create serverless application and deploy it.
- the CLI tool made by Node.js.

## How To Set Up
```
$ npm install -g serverless
$ serverless --version
$ serverless create --template aws-nodejs --name sample-app --path sample-app-directory
```

## Terms
- Provider : Cloud service which you will use. For example, AWS, GCP, Azure.
- Service : Environment to run the application.

## Templates
- aws-nodejs
- aws-nodejs-typescript
- aws-nodejs-ecma-script
- aws-python
- aws-python3
- aws-kotlin-jvm-maven
- aws-kotlin-jvm-gradle
- aws-kotlin-nodejs-gradle
- aws-groovy-gradle
- aws-java-maven
- aws-java-gradle
- aws-scala-sbt
- aws-csharp
- aws-fsharp

## Files
- `serverless.yml`
- `handler.js`
- `event.json` : Define values to input running function.

## Reference
- [Serverless Operations blog : Serverless Frameworkの使い方まとめ](https://serverless.co.jp/blog/25/)
