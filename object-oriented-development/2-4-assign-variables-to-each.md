## Sample After 2-3
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

## Assign Variables To Each
We can reduce the possibility to affect unintended influences on the variable when we use the same variable for many times and everywhere.
Needless to say, we can read code more easily.

```php
public function getTotalPrice(int $quantity, int $unitPrice): int
{
  $basePrice = $quantity * $unitPrice;

  $shippingCost = 0;

  if ($basePrice < 3000) {
    $shippingCost += 500;
  }

  $totalPrice = ($basePrice + $shippingCost) * 1.1;

  return $totalPrice;
}
```

## Reference
- 
