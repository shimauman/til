## Version
- 

## Premise
schools table
id | name
-- | --
1 | school1
2 | school2

```
>>> $school = School::where('id', 1)->get();

=> Illuminate\Database\Eloquent\Collection {#3477
     all: [
       App\Models\School {#3482
         id: 1,
         name: "school1",
       },
     ],
   }
```

## `all`
```
>>> $school = School::where('id', 1)->get()->all();

=> [
     App\Models\School {#3498
       id: 1,
       name: "school1",
     },
   ]
```

## `toArray`
```
>>> $school = School::where('id', 1)->get()->toArray();

=> [
     [
       "id" => 1,
       "name" => "school1",
     ],
   ]
>>>
```

## Caution
```php
// [1,2,3]
collect([1, 2, 3])->all();
collect([1, 2, 3])->toArray();
```
```php
// ["name" => "Desk", "price" => 10000]
collect(['name' => 'Desk', 'price' => 10000])->all();
collect(['name' => 'Desk', 'price' => 10000])->toArray();
```

## Reference
- [Laravel8.x公式 : コレクション - all()](https://readouble.com/laravel/6.x/ja/collections.html)
- [Laravel8.x公式 : コレクション - toArray()](https://readouble.com/laravel/8.x/ja/collections.html#method-toarray)
