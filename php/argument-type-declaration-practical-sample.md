## Version
- 

## Bad Sample
This sample has possibility to get number which isn't customer id and string which isn't formatized date. If there isn't `customer_id = 1000`, but this method can get and use the number.
```php
public function sampleMethod(int $customerId, string $rolledDate): Collection
{
    return $this
      ->model
      ->where('id', $customerId)
      ->where('rolled_date', $rolledDate)
      ->get();
}
```

## Too Much Sample
We can make CustomerId class and RolledDate class and use their instances. However, this sample is too much because we have to have and maintain more classes and test code.
```php
public function sampleMethod(CustomerId $customerId, RolledDate $rolledDate): Collection
{
    return $this
      ->model
      ->where('id', $customerId->getId())
      ->where('rolled_date', $rolledDate->getDate())
      ->get();
}
```

## Practical Sample
As practical sample, we can use Customer model class and Carbon class instances. We can remove possibility to get invalid type argument.
```php
public function sampleMethod(Customer $customer, Carbon $rolledDate): Collection
{
    return $this
      ->model
      ->where('id', $customer->id)
      ->where('rolled_date', $rolledDate->toDateString())
      ->get();
}
```

## Reference
- 