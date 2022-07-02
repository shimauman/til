## Version
- 

## Drop Element(s) From Array

### Format
#### Unset
```php
unset(mixed $var, mixed ...$vars): void
```

#### Splice
```php
array_splice(
    array &$array,
    int $offset,
    ?int $length = null,
    mixed $replacement = []
): array
```

### Example
```php
// We want to drop 2
$array = [1,2,3];

$targetIndex = array_search(2, $array);
```

#### Unset
```php
// $array = [0 => 1, 2 => 3]
unset($array[$targetIndex]);

// $array = [0 => 1, 1 => 3]
$array = array_values($array);
```

#### Splice
```php
// $array = [0 => 1, 1 => 3]
array_splice($array, $targetIndex, 1);

// $droppedElements = [0 => 2]
$droppedElements = array_splice($array, $targetIndex, 1);
```

### Reference
- [PHP official document : unset](https://www.php.net/manual/ja/function.unset.php)
- [PHP official document : array_splice](https://www.php.net/manual/ja/function.array-splice.php)


## Get Sliced Array
### Format
```php
array_slice(
    array $array,
    int $offset,
    ?int $length = null,
    bool $preserve_keys = false
): array
```
### Example
```php
$array = array(1,2,3,4,5);
```
```php
// [ 0 => 3, 1 => 4, 2 => 5]
$slicedArray = array_slice($array, 2);
```
```php
// [ 0 => 4, 1 => 5]
$slicedArray = array_slice($array, -2);
```
```php
// [ 0 => 3 ]
$slicedArray = array_slice($array, 2, 1);
```
```php
// [ 0 => 4 ]
$slicedArray = array_slice($array, -2, 1);
```
```php
// [ 2 => 3, 3 => 4, 4 => 5]
$slicedArray = array_slice($array, 2, null, true);
```
### Reference
- [PHP official document : array_slice](https://www.php.net/manual/ja/function.array-slice.php)


## Create Array With Range
### Format
```php
range(string|int|float $start, string|int|float $end, int|float $step = 1): array
```

### Example
```php
// [1,2,3,4,5]
range(1, 5);
```
```php
// [0,10,20,30,50]
range(0, 50, 10);
```
```php
// ['a', 'b', 'c', 'd']
range('a', 'd');
```
```php
// ['a', 'c', 'e']
range('a', 'e', 2);
```
```php
// ['c', 'b', 'a']
range('c', 'a');
```

### Reference
 - [PHP official document : range](https://www.php.net/manual/ja/function.range.php)



## Join Array Elements
### Format
```php
implode(string $separator, array $array): string
```

### Example
```php
// '1,2,3,4,5,6'
implode(',', [1,2,3,4,5,6]);
```
```php
// '123456'
implode([1,2,3,4,5,6]);
```
```php
// ''
implode(',', array());
```

### Reference
 - [PHP official document : implode](https://www.php.net/manual/ja/function.implode.php)


## Remove String
### Format
```php
substr(string $string, int $offset, ?int $length = null): string
```

### Example
```php
$sample = "abcde";

// bcde
echo substr($sample,1);

// bcd
echo substr($sample,1,3);

// abcde
echo substr($sample);
```
```php
$sample = "あいうえお";

// あい
echo mb_substr($sample,0,2);
```

### Reference
 - [PHP official document : substr](https://www.php.net/manual/ja/function.substr.php)


## File Manipulations
### Format
#### Copy File
```php
copy (string $source, string $dest, resource $context = ?) : bool
```
- `dest` : Destination.

#### Remove File
```php
unlink (string $filename, resource $context = ?) : bool
```

### Reference
 - [PHP official document : copy](https://www.php.net/manual/ja/function.copy.php))
 - [PHP official document : unlink](hhttps://www.php.net/manual/ja/function.unlink.php)


## Get Hash Value Of The File
### Format
```php
hash_file (string $algo, string $filename, bool $binary = false) : string|false
```
- `algo` : Hash algorithm.

### Example
```php
<?php
file_put_contents('example.txt', 'The quick brown fox jumped over the lazy dog.');

// b7273c05ad141ccb6696b3659e57137c453b6d64690fa7d5cf96368df4a7138703a8c6ead31727b487b3628746510391
echo hash_file('sha384', 'example.txt');

// '<feW|E;mdiϖ6'bFQ
echo hash_file('sha384', 'example.txt', true);
?>
```
### Reference
 - [PHP official document : hash_file](https://www.php.net/manual/ja/function.hash-file.php)
