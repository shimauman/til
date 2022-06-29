## Version
- 

## Reset Key
```php
// collect([1,2])
collect([2 => 1, 4 => 2])->values();
```

## Make Unique
```php
// collect([0 => 1, 1 => 2, 3 => 3])
collect([1,2,2,3])->unique();

↓

// collect([0 => 1, 1 => 2, 2 => 3])
collect([1,2,2,3])->unique()->values();
```

## Collect Values Of Specific Key
```php
// collect(['taro', 'hanako'])
collect([
    ['id' => 1, 'name' => 'taro'],
    ['id' => 2, 'name' => 'hanako'],
])->pluck('name');
```

## Reference
- [Laravel6.x公式 : コレクション](https://readouble.com/laravel/6.x/ja/collections.html)
