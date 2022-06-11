## Sample After 2-4
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

## Extract As Method
If we extract logic to decide shipping cost as a method, we can lock the logic in the method.
This enables us to update the logic easily and improve readbility of code which calls the method.

```php
public function getTotalPrice(int $quantity, int $unitPrice): int
{
  $basePrice = $quantity * $unitPrice;

  $shippingCost = $this->getShippingCost($basePrice);

  $totalPrice = ($basePrice + $shippingCost) * 1.1;

  return $totalPrice;
}

public function getShippingCost(int $basePrice): int
{
  if ($basePrice < 3000) {
    return 500;
  }

  return 0;
}
```

## Reference
- 
