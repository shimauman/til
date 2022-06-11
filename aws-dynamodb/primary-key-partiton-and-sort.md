## Version
- 

## Primary Key
- Primary key is the key which can specify only one record.
- We can use partition key or partition key and sort key as primary key.
- Ascending order is used in sort key.

## Sample
- "School" is partition key.
- "Grade" is sort key.

Partition
```json
{
  "School": "A School",
  "Grade": "1",
}

{
  "School": "A School",
  "Grade": "2",
}

{
  "School": "A School",
  "Grade": "3",
}
```

Partition
```json
{
  "School": "B School",
  "Grade": "1",
}

{
  "School": "B School",
  "Grade": "2",
}
```

Partition
```json
{
  "School": "C School",
  "Grade": "1",
}
```

## Reference
- [AWS official docs : Partitions and Data Distribution](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/HowItWorks.Partitions.html)
