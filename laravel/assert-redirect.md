## Version
- 

## How To
In feature test method,

### Check redirecting

```php
$indexPageUri = route(***);
$storeUri = route(***);

$response = $this->post($storeUri);

$response->assertStatus(302);
$response->assertRedirect($indexPageUri);

$this->get($indexPageUri)->assertSeeText('message');
```

### Check redirecting by validation errors
```php
$indexPageUri = route(***);
$storeUri = route(***);

$response = $this
  ->from($indexPageUri)
  ->post($storeUri);

$response->assertStatus(302);
$response->assertRedirect($indexPageUri);
```

## `assertRedirect`
This method checks only redirecting to the URI. Not go to the URI actually.

## Reference
- [laravel 8.x official document assertRedirect](https://readouble.com/laravel/8.x/en/http-tests.html#assert-redirect)
- [laravel 8.x official document assertSeeText](https://readouble.com/laravel/8.x/en/http-tests.html#assert-see-text)
