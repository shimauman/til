## Version
- 

## Sample
```js
const AWS = require('aws-sdk');
// When we use Dynamo DB on local.
const dynamodbClient = new AWS.DynamoDB.DocumentClient({
  region: 'localhost',
  // If port is 8000.
  endpoint: 'http://localhost:8000',
  // If necessary.
  accessKeyId: process.env.ACCESS_KEY_ID,
  // If necessary.
  secretAccessKey: process.env.ACCESS_KEY_ID
});

***
```

## Reference
- [Serverless official docs : Using DynamoDB Local in your code](https://www.serverless.com/plugins/serverless-dynamodb-local)
