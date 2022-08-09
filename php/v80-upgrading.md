## Version
- PHP v8.0.0

## Named Arguments

### PHP v7
```php
htmlspecialchars($string, ENT_COMPAT | ENT_HTML401, 'UTF-8', false);
```

### PHP v8.0
```php
htmlspecialchars($string, double_encode: false);
```

## Constructor Property Promotion
### PHP v7
```php
class Point {
  public float $x;
  public float $y;
  public float $z;

  public function __construct(
    float $x = 0.0,
    float $y = 0.0,
    float $z = 0.0
  ) {
    $this->x = $x;
    $this->y = $y;
    $this->z = $z;
  }
}
```

### PHP v8.0
This is a little difficult to check properties the class has.

```php
class Point {
  public function __construct(
    public float $x = 0.0,
    public float $y = 0.0,
    public float $z = 0.0,
  ) {}
}
```

## Union Types
### PHP v7
```php
class Number {
  /** @var int|float */
  private $number;

  /**
   * @param float|int $number
   */
  public function __construct($number) {
    $this->number = $number;
  }
}

new Number('NaN'); // OK
```

### PHP v8.0
```php
class Number {
  public function __construct(
    private int|float $number
  ) {}
}

new Number('NaN'); // TypeError
```

## Match Expression
### PHP v7
```php
switch (8.0) {
  case '8.0':
    $result = "Oh no!";
    break;
  case 8.0:
    $result = "This is what I expected";
    break;
}
echo $result; // Oh no!
```

### PHP v8.0
- Match is an expression, meaning its **result can be stored in a variable or returned.**
- Match branches **only support single-line expressions** and do **not need a `break;` statement**.
- Match does **strict comparisons**.
```php
echo match (8.0) {
  '8.0' => "Oh no!",
  8.0 => "This is what I expected",
};
```

## Nullsafe Operator
### PHP v7
```php
$country =  null;

if ($session !== null) {
  $user = $session->user;

  if ($user !== null) {
    $address = $user->getAddress();

    if ($address !== null) {
      $country = $address->country;
    }
  }
}
```

### PHP v8.0
When the evaluation of one element in the chain fails, the execution of the entire chain **aborts** and the entire chain **evaluates to null**.
```php
$country = $session?->user?->getAddress()?->country;
```

## Saner String To Number Comparisons
### PHP v7
```php
0 == 'foobar' // true
```

### PHP v8.0
```php
0 == 'foobar' // false
```

## Removed ability to call non-static methods statically.
```php
class Foo {
    public function bar() {}
}

Foo::bar();
```
### PHP v7
```
Deprecated: Non-static method Foo::bar() should not be called statically
```

### PHP v8.0
```
Fatal error: Uncaught Error: Non-static method Foo::bar() cannot be called statically
```


## The precedence of the concatenation operator has changed.
```php
$count = 1;

echo 'total count is ' . $count + 1;
```
### PHP v7
```
PHP Deprecated:  The behavior of unparenthesized expressions containing both '.' and '+'/'-' will change in PHP 8: '+'/'-' will take a higher precedence
```

### PHP v8.0
- `+` / `-` will take a higher precedence.
```
total count is 2
```

## Arguments with a default value that resolves to null at runtime will no longer implicitly mark the argument type as nullable.
```php
const RESOLVING_TO_NULL = null;

function foo(int $argument = RESOLVING_TO_NULL) {}
```

### PHP v7
No Error

### PHP v8.0
```
Fatal error: Uncaught TypeError: foo(): Argument #1 ($argument) must be of type int, null given
```

## Reference
- [GitHub php/php-src v8.0.0](https://github.com/php/php-src/blob/php-8.0.0/UPGRADING)
- [PHP official docs : releases v8.0.0](https://www.php.net/releases/8.0/en.php)
- [Qiita : PHP8.0がリリースされたので新機能全部やる](https://qiita.com/rana_kualu/items/c110cb244c3ee38c6859)
