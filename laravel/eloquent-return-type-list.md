## Version
- 

schools table
id | name
-- | --
1 | school1
2 | school2

## Summary
method | return type
-- | --
`find` | School model instance
`first` | School model instance
`get` | Collection instance - includes School model instance
`all` | Collection instance - includes School model instance
`where` | Builder instance

## `find`
```
>>> $school = School::find(1);

=> App\Models\School {#3488
     id: 1,
     name: "school1",
   }
```

## `first`
```
>>> $school = School::where('id', 1)->first();

=> App\Models\School {#3498
     id: 1,
     name: "school1",
   }
```

## `get`
```
>>> $school = School::where('id', 1)->get();

=> Illuminate\Database\Eloquent\Collection {#3488
     all: [
       App\Models\School {#3492
         id: 1,
         name: "school1",
       },
     ],
   }
```
```
>>> $school = School::where('id', 1)->get()->all();

=> [
     App\Models\School {#3498
       id: 1,
       name: "school1",
     },
   ]
```

## `all`
```
>>> $school = School::all();

=> Illuminate\Database\Eloquent\Collection {#3499
     all: [
       App\Models\School {#3471
         id: 1,
         name: "school1",
       },
       App\Models\School {#3496
         id: 2,
         name: "school2",
       },
     ],
   }
```

## `where`
```
>>> $school = School::where('id', 1);

=> Illuminate\Database\Eloquent\Builder {#3477}
```

## Reference
- [Laravel6.x公式 : Eloquent](https://readouble.com/laravel/6.x/ja/eloquent.html)
- [Qiita : 返り値早見表](https://qiita.com/sola-msr/items/fac931c72e1c46ae5f0f)
