## Version
- AWS SDK v2

## Sample
```js
const AWS = require('aws-sdk');
const dynamodbClient = new AWS.DynamoDB.DocumentClient();

const params = {
    TableName: 'User',
    Key:{
      name: 'User 1',
    }
};

// Way1 : Using call back.
dynamodbClient.get(params, function(error, data) {
  if (error) {
    console.log('Error', error);
  } else {
    console.log('Success', data.Item);
  }
});

// Way2 : Using async / await.
async () => {
  try {
    const results = await dynamodbClient.get(params).promise();
    console.log('Success', data.Item);
  } catch (error) {
    console.log('Error', error);
  }
}
```

## Reference
- [AWS official docs : Using the Dynamo DB Document Client](https://docs.aws.amazon.com/sdk-for-javascript/v2/developer-guide/dynamodb-example-document-client.html)
