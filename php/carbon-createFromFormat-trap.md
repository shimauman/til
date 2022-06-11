## Version
- 

## Trap of `createFromFormat`
If today is `2022.03.31`.

```php
Carbon::createFromFormat('Y-m', '2022-02');
```
This code makes `2022-03-01` carbon instance because `2022-02-31` does not exist.

## Solution
If you don't use `day` data in code after the `createFromFormat`,

```php
Carbon::createFromFormat('Y-m-d', '2022-02-01');
```

## Reference
- 
