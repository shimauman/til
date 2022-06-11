## Version
laravel 5.x - 8.x

## Before Using @forelse
```php
@if ($posts->isNotEmpty())
    @foreach ($posts as $post)
        <span>{{ $post->title }}</span>
    @endforeach
@else
    <p>There are no posts.</p>
@endif
```

## After Using @forelse
```php
@forelse ($posts as $post)
    <span>{{ $post->title }}</span>
@empty
    <p>There are no posts.</p>
@endforelse
```

## Reference
- [blade templates](https://readouble.com/laravel/8.x/en/blade.html)