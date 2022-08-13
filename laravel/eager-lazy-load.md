## Version
- 

Users table
id | name | is_active
-- | -- | --
1 | tanaka | 1
2 | sato | 1

Posts table
id | title | user_id
-- | -- | --
1 | first | 1
2 | second | 1
3 | third | 2

```php
class Post extends Model
{
  public function user(): BelongsTo
  {
    return $this->belongsTo(User::class)
  }
}
```

## Lazy Load
Load relational data only when the relational property is accessed.
```php
$posts = Post::all();

foreach ($posts as $post) {
  $user = $post->user;
}
```

### N+1 Query Problem
```php
// 1 query
$posts = Post::all();

foreach ($posts as $post) {
  // Query for numbers of posts
  echo $post->user->name;
}
```

## Eager Load
```php
$posts = Post::with('user')->get();

foreach ($posts as $post) {
  echo $post->user->name;
}
```

### Solve N+1 Problem
```php
// 2 queries :
// The query to get all posts
// and the another query to get all users who have the posts.
$posts = Post::with('user')->get();

foreach ($posts as $post) {
  echo $post->user->name;
}
```

## Tips

### What Is Dynamic Property?
```php
// user is dynamic property because it is not fixed property but depends on relation.
$post->user->name;
```

### Relation Method Can Be Used As Query Builder
```php
$post->user()->where('is_active', 1)->get();
```

## Reference
- [Laravel readouble : Laravel8.x Eloquent](https://readouble.com/laravel/8.x/en/eloquent-relationships.html#eager-loading)
- [LaravelのEagerLoadまとめ。動的プロパティとEloquentリレーションの違いなど](https://katsusand.dev/posts/laravel-eager-load/)
