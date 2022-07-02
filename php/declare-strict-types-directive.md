## Version
- 

## Declare Strict Types Directive
Check type strictly.
```php
declare(strict_types=1);
```

```php
<?php
declare(strict_types=1);

function sum(int $first, int $second): int
{
    return $first + $second;
}

// int(3)
var_dump(sum(1,2));

// PHP Fatal error:  Uncaught TypeError: Argument 1 passed to sum() must be of the type int, float given...
var_dump(sum(1.5, 2.5));
```

## NOTE
### 1. `Int` can be considered as `float`
```php
<?php
declare(strict_types=1);

function sum(float $first, float $second) {
    return $first + $second;
}

// float(3)
var_dump(sum(1,2));
```

### 2. Influence
Can only influence for code written in file with `declare`.

### 3. Directive Value
As directives are handled as the file is being compiled, only literals may be given as directive values. Variables and constants cannot be used.
```php
<?php
// OK
declare(strict_type=1);

// NG
const STRICT_TYPE = 1;
declare(STRICT_TYPE);
```

## Reference
- [PHP official doc : 型宣言](https://www.php.net/manual/ja/language.types.declarations.php#language.types.declarations.strict)
- [PHP official doc : declare](https://www.php.net/manual/ja/control-structures.declare.php)
- [Qiita : declare(strict_types=1)の効力範囲](https://qiita.com/Hiraku/items/734f0666ab3d34c52efa)
