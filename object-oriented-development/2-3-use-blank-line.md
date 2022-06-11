## Sample After 2-2
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

## Use Blank Line
Separating code by blank line enables us to read it easily.

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
