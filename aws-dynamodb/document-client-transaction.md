## Version
- 

## Sample
```js
const params = {
  TransactItems: [{
    Put: {
      TableName : 'Table0',
      Item: {
        HashKey: 'haskey',
        NumAttribute: 1,
        BoolAttribute: true,
        ListAttribute: [1, 'two', false],
        MapAttribute: { foo: 'bar'},
        NullAttribute: null
      }
    }
  }, {
    Update: {
      TableName: 'Table1',
      Key: { HashKey : 'hashkey' },
      UpdateExpression: 'set #a = :x + :y',
      ConditionExpression: '#a < :MAX',
      ExpressionAttributeNames: {'#a' : 'Sum'},
      ExpressionAttributeValues: {
        ':x' : 20,
        ':y' : 45,
        ':MAX' : 100,
      }
    }
  }]
};

documentClient.transactWrite(params, function(err, data) {
  if (err) console.log(err);
  else console.log(data);
});
```

## Reference
- [AWS Dynamo DB Document Class List : transactWrite](https://docs.aws.amazon.com/AWSJavaScriptSDK/latest/AWS/DynamoDB/DocumentClient.html#transactWrite-property)
