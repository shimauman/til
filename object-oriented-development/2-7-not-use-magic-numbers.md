## Sample (`ShippingCost`) After 2-6
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

## Not Use Magic Numbers
Magic numbers are the numbers which appear in code suddenly.
They decrease maintenability and readability.

### If we use magic numbers
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

  public function ***(): ***
  {
    ***
    *** 3000 ***
    ***
  }

  public function ***(): ***
  {
    ***
    *** 500 ***
    ***
  }
}
```

### No magic numbers
If we have to change shipping cost amount, we just change only one line.

```php
class ShippingCost()
{
  private const MINIMUM_FOR_FREE = 3000;
  private const COST = 500;
  private const MINIMUM_COST = 0;

  private int $basePrice;

  public function __construct(int $basePrice)
  {
    $this->basePrice = $basePrice;
  }

  public function getCost(): int
  {
    if ($this->basePrice < self::MINIMUM_FOR_FREE) {
      return self::COST;
    }

    return self::MINIMUM_COST;
  }

  public function ***(): ***
  {
    ***
    *** self::MINIMUM_FOR_FREE ***
    ***
  }

  public function ***(): ***
  {
    ***
    *** self::COST ***
    ***
  }
}
```

## Reference
- 
