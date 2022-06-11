## Version
- 

## Sample
```js
const AWS = require("aws-sdk");
dbClient = new AWS.DynamoDB({ region: 'ap-northeast-1' });

const run = async () => {
  try {
    // add promise as last chain.
    const results = await dbClient.listTables({}).promise();
    console.log(results.TableNames.join("\n"));
  } catch (err) {
    console.error(err);
  }
};
run();
```

## Reference
- [AWS official docs : using async/await](https://docs.aws.amazon.com/sdk-for-javascript/v2/developer-guide/using-async-await.html)
