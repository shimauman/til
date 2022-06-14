## Version
- 

## Setting In `serverless.yml`
Add IAM role on the Lambda function.

```yml
// serverless.yml

provider:
  // Other settings

  iam:
    role:
      statements:
        - Effect: 'Allow'
          Action:
            - 'dynamodb:*'
          Resource:
            - 'arn:aws:dynamodb:ap-northeast-1:*:table/User'
            - 'arn:aws:dynamodb:ap-northeast-1:*:table/Sample'
```

## Without Setting
```
{
  "errorType": "AccessDeniedException",
  "errorMessage": "User: arn:aws:sts::************:assumed-role/***-***-dev-ap-northeast-1-lambdaRole/sample-function is not authorized to perform: dynamodb:Scan on resource: arn:aws:dynamodb:ap-northeast-1:************:table/User because no identity-based policy allows the dynamodb:Scan action",
```

## Reference
- [Serverless Framework Documentation : IAM Permissions For Functions](https://www.serverless.com/framework/docs/providers/aws/guide/iam)
