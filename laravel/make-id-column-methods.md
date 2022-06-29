TODO: 情報を追加していく。

## Version
- 

## Making ID Column Methods
```php
// bigIncrements, 'id' column
$table->id()
```
```php
// bigIncrements, UNSIGNED BIGINT
$table->bigIncrements('id');
```
```php
// increments, UNSIGNED INTEGER
$table->increments('id')
```
```php
// increments, INTEGER
$table->integer('id')->autoIncrement()
```

## Reference
- [Laravel8.x公式 : マイグレーション](https://readouble.com/laravel/8.x/ja/migrations.html)
