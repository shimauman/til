## Version
- PHP v7.4

## Property Type Declaration
```php
class User
{
  private string $name = 'default name';
  private ?int $nickName = null;
  private int $age;
}
```

## Arrow Function
```php
$array = [1, 2, 3];

$doubledArray = array_map(fn($each) => $each * 2, $array);
```
```php
$double = fn($value) => $value * 2;

$double(1);
```

## Nullish coalescing operator (Null合体演算子)

```php
$a = null;
$a ??= 'hoge';

echo $a; // hoge
```

```php
$a ??= 'hoge';

echo $a; // hoge
```

```php
$a = 1;
$a ??= 'hoge';

echo $a; // 1
```

## `mb_str_split`
```php
$x = mb_str_split('aAａＡ1１!！あ𩸽', 1);

// ['a', 'A', 'ａ', 'Ａ', '1', '１', '!', '！', 'あ', '𩸽']
var_export($x);
```

```php
$x = mb_str_split('aAａＡ1１!！あ𩸽', 2);

// ['aA', 'ａＡ', '1１', '!！', 'あ𩸽']
var_export($x);
```

```php
$x = mb_str_split('aAａＡ1１!！あ𩸽', 3);

// ['aAａ', 'Ａ1１', '!！あ', '𩸽']
var_export($x);
```

```php
$x = mb_str_split(12345, 1);

// ['1', '2', '3', '4', '5']
var_export($x);
```

## Unpack Array In Array
```php
$parts = ['apple', 'pear'];

// ['banana', 'orange', 'apple', 'pear', 'watermelon'];
$fruits = ['banana', 'orange', ...$parts, 'watermelon'];
```

## Reference
- [Qiita : PHP7.4がリリースされたので新機能全部やる](https://qiita.com/rana_kualu/items/50f9f5735321fe995ff5)
