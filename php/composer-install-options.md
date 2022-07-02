## Version
- 

## Options
```
composer install ***
```
- `--verbose` : `-v`. Show detail(name and version) of installed packages.
- `--prefer-dist` : Download as zip.
- `--prefer-source` : Download via git clone.
- `--no-progress` : Undisplay download progress.
- `--no-interaction` : Undisplay interactive message.
- `--no-dev` : Only install `require` packages written in `composer.json`.
- `--optimize-autoloader` : Accelerate autoloader.
- `--no-suggest` : No output names of suggested packages.

## Terms
- `autoloader` : Which can auto load php file. We can load all php files with `require_once "vendor/autoload.php";`.
- `suggest` : Installed packages sometimes have suggested packages.

## Use Case
When we show only necessary information.
```
RUN composer install --verbose --prefer-dist --no-progress --no-interaction --no-dev --optimize-autoloader --no-suggest
```

## Reference
 - 
