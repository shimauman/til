## Version
- 

## Sample Without `copy` Method

```
>>> $currentDate = Carbon::parse('2020-01-01');
=> Carbon\Carbon @1577836800 {#3554
     date: 2020-01-01 00:00:00.0 UTC (+00:00),
   }

>>> $currentDate->addDay();
=> Carbon\Carbon @1577923200 {#3554
     date: 2020-01-02 00:00:00.0 UTC (+00:00),
   }

>>> echo $currentDate;
2020-01-02 00:00:00
```

## Sample With `copy` Method

> You can also create a copy() of an existing Carbon instance. As expected the date, time and timezone values are all copied to the new instance.

```
>>> $currentDate = Carbon::parse('2020-01-01');
=> Carbon\Carbon @1577836800 {#3537
     date: 2020-01-01 00:00:00.0 UTC (+00:00),
   }

>>> $currentDate->copy()->addDay();
=> Carbon\Carbon @1577923200 {#3543
     date: 2020-01-02 00:00:00.0 UTC (+00:00),
   }

>>> echo $currentDate;
2020-01-01 00:00:00
```

## Reference
- [carbon official document](https://carbon.nesbot.com/docs/)
