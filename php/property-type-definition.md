## Version
- PHP v7.4

## Before v7.4
```php
class Sample
{
    /**
     * @var SampleRepository
     */
    private $sampleRepository;
}
```

## After v7.4
```php
class Sample
{
    private SampleRepository $sampleRepository;
}
```

## Reference
- [PHP official document : Migrating from PHP 7.3.x to PHP 7.4.x](https://www.php.net/manual/en/migration74.new-features.php)
