## Sample (`getTotalPrice()`) After 2-6
```php
public function getTotalPrice(int $quantity, int $unitPrice): int
{
  $basePrice = $quantity * $unitPrice;

  $shippingCost = (new ShippingCost($basePrice)->getCost());

  $totalPrice = ($basePrice + $shippingCost) * 1.1;

  return $totalPrice;
}
```

## Make Value Object
Primitive type like int, string, array have posiibility to get unintended values.
For example, user can select value between `1` <= `$quantity` <= `100` in our system.
However, `getTotalPrice()` can get `0` and `101` as `$quantity`. So, we make `Quantity` class.

```php
class Quantity
{
  private const MIN = 1;
  private const MAX = 100;

  private int $quantity;

  public function __construct(int $value)
  {
    if ($value < self::MIN || $value > self::MAX) {
      throw new InvalidQuantityException($value);
    }

    $this->quantity = $value;
  }
}
```
```php
// Somewhere...
***
->getTotalPrice(new Quantity($inputQuantity), $unitPrice);
***

public function getTotalPrice(Quantity $quantity, int $unitPrice): int
{
  $basePrice = $quantity * $unitPrice;

  $shippingCost = (new ShippingCost($basePrice)->getCost());

  $totalPrice = ($basePrice + $shippingCost) * 1.1;

  return $totalPrice;
}
```

## Reference
- 
