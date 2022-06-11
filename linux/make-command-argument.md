## Version
-

## How To Give Command Argument
```Makefile
LINT_TARGET := ./

lint:
  ./vendor/bin/phpcs --standard=phpcs.xml ${LINT_TARGET}
```

```
$ make lint LINT_TARGET=./sample/sample.php
```

## Reference
- 
