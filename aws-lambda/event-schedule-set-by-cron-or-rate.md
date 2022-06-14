## Version
- 

## With Cron
```
cron(Miniutes, Hours, Day of month, Month, Day of week, Year)
```
```
cron(30 11 * * ? *) // 11:30(UTC) everyday

cron(30 2 * * ? *) // 11:30(JST) every day

cron(30 11 1 * ? *) // 11:30(UTC) on first day of every month

cron(30 11 ? * 2#1 *) // 11:30(UTC) on first Monday of every month

cron(30 11 ? * Mon-FRI *) // 11:30(UTC) on Mon - Fri every week

cron(0/30 * ? * Mon-FRI *) // Every 30 miniutes on Mon - Fri every week

cron(0/5 8-17 ? * Mon-FRI *) // Every 5 miniutes(8:00 - 17:55) on Mon - Fri every week
```

## With Rate
```
rate(5 miniutes) // Every 5 miniutes

rate(1 hour) // Every 1 hour

rate(7 days) // Every 7 days
```


## Reference
- [AWS Official Documentation : Schedule expressions using rate or cron](https://docs.aws.amazon.com/lambda/latest/dg/services-cloudwatchevents-expressions.html)
