## Version
laravel 5.x - 8.x

## Use Paginator Class
```php
new Paginator(
  mixed $items,
  int $perPage,
  int|null $currentPage,
  array $options (path, query, fragment, pageName)
)
```

### Example
```php
use Illuminate\Pagination\Paginator;

public function makePaginationFromArray (***, Request $request): Paginator
{
  ***

  $items = [
    [***],
    ***
  ];

  $currentPageIndex = $request->page ? $request->page - 1 : 0;
  $itemsCountPerPage = 20;

  return new LengthAwarePaginator(
    array_slice($items, $currentPageIndex * $itemsCountPerPage, $itemsCountPerPage),
    $itemsCountPerPage,
    $request->page,
    [
      'path' => route('***', [
        '***' => $***,
      ])
    ]
  );
}
```

### UI
Pagination has only previous and next page link display.


## Use LengthAwarePaginator Class
```php
new LengthAwarePaginator(
  mixed $items,
  int $total,
  int $perPage,
  int|null $currentPage,
  array $options (path, query, fragment, pageName)
)
```

### Example
```php
use Illuminate\Pagination\LengthAwarePaginator;

public function makePaginationFromArray (***, Request $request): LengthAwarePaginator
{
  ***

  $items = [
    [***],
    ***
  ];

  $currentPageIndex = $request->page ? $request->page - 1 : 0;
  $itemsCountPerPage = 20;

  return new LengthAwarePaginator(
    array_slice($items, $currentPageIndex * $itemsCountPerPage, $itemsCountPerPage),
    count($items),
    $itemsCountPerPage,
    $request->page,
    [
      'path' => route('***', [
        '***' => $***,
      ])
    ]
  );
}
```

### UI
Pagination has each page link display.

## Reference
- [laravel 8.x Paginator class description](https://laravel.com/api/8.x/Illuminate/Pagination/Paginator.html)
- [laravel 8.x LengthAwarePaginator class description](https://laravel.com/api/8.x/Illuminate/Pagination/LengthAwarePaginator.html)
- [laravel 8.x Paginator class source code](https://github.com/laravel/framework/blob/8.x/src/Illuminate/Pagination/Paginator.php)
- [laravel 8.x LengthAwarePaginator class source code](https://github.com/laravel/framework/blob/8.x/src/Illuminate/Pagination/LengthAwarePaginator.php)