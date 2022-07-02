## Version
- 

## `$_SERVER`
> This is a 'superglobal', or automatic global, variable. This simply means that it is available in all scopes throughout a script. There is no need to do global $variable; to access it within functions or methods.

> $_SERVER is an array containing information such as headers, paths, and script locations. The entries in this array are created by the web server. There is no guarantee that every web server will provide any of these; servers may omit some, or provide others not listed here. That said, a large number of these variables are accounted for in the [CGI/1.1 specification](http://www.faqs.org/rfcs/rfc3875.html), so you should be able to expect those.

## Usage
```php
// www.example.com
echo $_SERVER['SERVER_NAME'];
```
```php
$_SERVER['NEW_KEY'] = 'new value';
```

## Reference
- [PHP official doc : $_SERVER](https://www.php.net/manual/en/reserved.variables.server.php)
