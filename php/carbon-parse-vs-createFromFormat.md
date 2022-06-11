## Version
- 

## `parse()`
`parse()` has possibility to make Carbon instance from unintended value.

```
>>> use Carbon\Carbon;

>>> $parsedDate = Carbon::parse(null);
=> Carbon\Carbon @1642135340 {#3546
     date: 2022-01-14 04:42:20.921077 UTC (+00:00),
   }

>>> $parsedDate = Carbon::parse(0);
=> Carbon\Carbon @0 {#3561
     date: 1970-01-01 00:00:00.0 +00:00,
   }

>>> $parsedDate = Carbon::parse('string');
<warning>PHP Warning:  DateTime::modify(): Failed to parse time string (string) at position 0 (s): The timezone could not be found in the database in /work/backend/vendor/nesbot/carbon/src/Carbon/Traits/Modifiers.php on line 439</warning>
Carbon\Exceptions\InvalidFormatException with message 'Could not parse 'string': Failed to parse time string (string) at position 0 (s): The timezone could not be found in the database'

>>> $parsedDate = Carbon::parse('20000');
<warning>PHP Warning:  DateTime::modify(): Failed to parse time string (20000) at position 4 (0): Unexpected character in /work/backend/vendor/nesbot/carbon/src/Carbon/Traits/Modifiers.php on line 439</warning>
Carbon\Exceptions\InvalidFormatException with message 'Could not parse '20000': Failed to parse time string (20000) at position 4 (0): Unexpected character'
```

## `createFromFormat()`
If we know the date format of the argument, we can use `createFromFormat()`.
This method doesn't make Carbon instance from the argument whose format is different from the format designed in 1st argument. So, We can reduce possibility to make Carbon instance from unintended value.

```
>>> use Carbon\Carbon;

>>> $createFromFormatedDate = Carbon::createFromFormat('Y-m-d', $formatedDate);
=> Carbon\Carbon @1577854110 {#3558
     date: 2020-01-01 04:48:30.0 UTC (+00:00),
   }

>>> $createFromFormatedDate = Carbon::createFromFormat('Y-m-d H:i:s', $formatedDate);
Carbon\Exceptions\InvalidFormatException with message 'Data missing'

>>> $createFromFormatedDate = Carbon::createFromFormat('Y-m', $formatedDate);
Carbon\Exceptions\InvalidFormatException with message 'Trailing data'

>>> $createFromFormatedDate = Carbon::createFromFormat('Y-m-d', 0);
Carbon\Exceptions\InvalidFormatException with message 'Data missing'

>>> $createFromFormatedDate = Carbon::createFromFormat('Y-m-d', null);
Carbon\Exceptions\InvalidFormatException with message 'Data missing'
```

## Reference
- [`parse()` source code](https://github.com/briannesbitt/Carbon/blob/master/src/Carbon/Traits/Creator.php#L211-L224)
- [`createFromFormat()` source code](https://github.com/briannesbitt/Carbon/blob/master/src/Carbon/Traits/Creator.php#L694-L706)