## Version
- 

## Sample
```php
$number = 10;
$first = 1;
$diff = 5;

echo(getSequenceNumber($number));

function getSequenceNumber(int $number): int
{
  global $first, $diff;

  return $first + $diff * ($number - 1);
}
```

## Reference
- 
