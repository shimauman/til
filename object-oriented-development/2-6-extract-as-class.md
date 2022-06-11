## Sample After 2-5
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

## Extract As Class
We can use the logic to get proper shipping cost from any where.
If we have to fix logic related to shipping cost, we just check only `ShippingCost` class.

```php
class ShippingCost()
{
  private int $basePrice;

  public function __construct(int $basePrice)
  {
    $this->basePrice = $basePrice;
  }

  public function getCost(): int
  {
    if ($this->basePrice < 3000) {
      return 500;
    }

    return 0;
  }
}
```

```php
public function getTotalPrice(int $quantity, int $unitPrice): int
{
  $basePrice = $quantity * $unitPrice;

  $shippingCost = (new ShippingCost($basePrice)->getCost());

  $totalPrice = ($basePrice + $shippingCost) * 1.1;

  return $totalPrice;
}
```

```php
public function ***(): ***
{
  $basePrice = ***;

  $shippingCost = (new ShippingCost($basePrice)->getCost());

  ***
}
```

## Reference
- 
