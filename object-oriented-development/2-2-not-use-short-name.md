## Sample
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

## Not Use Short Name
This is the first step to write program which we can read and change easily which is the goal of object oriented development.

```php
public function getTotalPrice(int $quantity, int $unitPrice): int
{
  $price = $quantity * $unitPrice;
  if ($price < 3000) {
    $price += 500;
  }
  $price = $price * 1.1;
  return $price;
}
```

## Reference
- 
