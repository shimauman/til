## Version
- 

## How To
Install composer v2.0.10.

```Dockerfile
FROM php:7.3.26-fpm

RUN ***
    ***
    php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
    php -r "if (hash_file('sha384', 'composer-setup.php') === '756890a4488ce9024fc62c56153228907f1545c228516cbf63f885e036d37e9a59d27d63f46af1d4d07ee0f76181c7d3') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
    php composer-setup.php --version=2.0.10
    php -r "unlink('composer-setup.php');"
```

### Appendix 1
```
php -r "{php command}"
```

### Appendix 2
We can check hash numbers for each composer version in the below link destination.


## Reference
- [getcomposer org docs : Download Composer](https://getcomposer.org/download/)
