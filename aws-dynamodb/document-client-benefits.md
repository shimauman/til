## Version
- 

## With Dynamo DB Document Client
```js
const AWS = require('aws-sdk');
const dynamodbClient = new AWS.DynamoDB.DocumentClient();

const params = {
    TableName: 'User',
    Item:{
      name: 'User 1',
      age: 20,
    }
};

dynamodbClient.put(params, callback);
```

## Without Dynamo DB Document Client
```js
const AWS = require('aws-sdk');
const dynamodb = new AWS.DynamoDB();

const params = {
    TableName: 'User',
    Item:{
      'name':{S: 'User 1'},
      'age':{N: 20},
    }
};

dynamodb.putItem(params, callback);
```

## Basic Methods To Access Table
When we use Document Client
- `get`
- `put`
- `update`
- `delete`

When we don't use Document Client
- `GetItem `
- `PutItem`
- `UpdateItem`
- `DeleteItem`

## Reference
- [AWS official docs : Using the DynamoDB Document Client](https://docs.aws.amazon.com/sdk-for-javascript/v2/developer-guide/dynamodb-example-document-client.html)
- [AWS official docs : Working with Items and Attributes](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/WorkingWithItems.html)
