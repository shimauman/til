## Version
- 

## Solution
```
$ COMPOSER_MEMORY_LIMIT=-1 composer command
```

```
// When run composer update
$ COMPOSER_MEMORY_LIMIT=-1 composer update
```

## See Current Memory Limit
```
php -r "echo ini_get('memory_limit').PHP_EOL;"
```

## Reference
- [Composer org doc : Memory limit errors](https://getcomposer.org/doc/articles/troubleshooting.md#memory-limit-errors)
