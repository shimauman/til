## Do you have these experiences in your tasks?
- You didn't know where the target code was.
- When you added only one change, you had to fix much other code.
- Your change had affected other code you didn't realize.

## The difficult program to read and change
have these features.
- Long method name
- Big class
- Requre many arguments

## Cause
Firstly, this was small method.
```php
class Sample()
{
  public function getTotalAmount(): int
  {
    return $this->count * $this->amount;
  }
}
```

↓

Next, added small change.
```php
public function getTotalAmount(): int
{
  if ($this->count >= self::MIN_COUNT_DISCOUNT_APPLICATION) {
    return $this->count * $this->amount * self::DISCOUNT_RATIO;
  }

  return $this->count * $this->amount;
}
```
↓

Repeated adding small changes...

↓

When we notice, this method had much code.
```php
public function getTotalAmount****(***, ***): int
{
  if ($this->count >= self::MIN_COUNT_DISCOUNT_APPLICATION) {
    return $this->count * $this->amount * self::DISCOUNT_RATIO;
  }

  if (***) {
    if (***) {
      ***
    } elseif (***) {
      ***
    } else {
      ***
    }
  }

  ***
  ***

  return $this->count * $this->amount;
}
```

## Reference
- 
