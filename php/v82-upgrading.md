TODO : Need to update.

## Version
- PHP v8.2

## Disjunctive Normal Form Types
We can use Union and Intersection type in same time.

```php
function foo(A | (B & C) | int $argument)
```

## True / False / Null Types
```php
public null $foo = null;

public function foo(false $bar): false {}

public function foo(true $bar): true {}
```

## Readonly Class
```php
readonly class Foo {
    public int $bar;
}

$foo = new Foo();
$foo->bar = 1;
$foo->bar = 2; // Illegal reassignment
$foo->foo = 3; // Illegal dynamic property
```

## Dynamic Properties
```php
class Foo {}

$foo = new Foo();
$foo->bar = 1; // OK (< PHP v8.2)
$foo->bar = 1; // Deprecated error
```

## Deprecate ${} String Interpolation
```php
$foo = 'foo';

"$foo" // OK
"{$foo}" // OK
"${foo}" // NG
"${$foo}" // NG
```

## Reference
- [PHP official docs : todo v8.2](https://wiki.php.net/todo/php82)
- [Qiita :【PHP8.2】PHP8.2の新機能](https://qiita.com/rana_kualu/items/e350b8ff80f929626eb9)
