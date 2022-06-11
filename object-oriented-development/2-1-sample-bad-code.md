## Sample
This is bad code because it is difficult to understand.
```php
public function getTotalPrice(int $qty, int $unitP): int
{
  $p = $qty * $unitP;
  if ($p < 3000) {
    $p += 500;
  }
  $p = $p * 1.1;
  return $p
}
```

## Reference
- 
