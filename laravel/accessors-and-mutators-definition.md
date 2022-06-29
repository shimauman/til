## Version
- 

users table
id | first_name | last_name
-- | -- | --
1 | taro | tanaka


## Define Accessors
Define data format when we get it.

```php
<?php

namespace App\Models;

use Illuminate\Database\Eloquent\Model;

class User extends Model
{
    // get{Attribute}Attribute
    public function getFirstNameAttribute(string $value): string
    {
        return ucfirst($value);
    }
}
```
```php
use App\Models\User;

$user = User::find(1);

// taro->Taro
$firstName = $user->first_name;
```
```php
public function getFullNameAttribute()
{
    return "{$this->last_name} {$this->first_name}";
}

// tanaka taro
$fullName = $user->full_name;
```

## Define Mutators
Define data format when we set it.

```php
<?php

namespace App\Models;

use Illuminate\Database\Eloquent\Model;

class User extends Model
{
    // set{Attribute}Attribute
    public function setFirstNameAttribute(string $value): void
    {
        $this->attributes['first_name'] = strtolower($value);
    }
}
```
```php
use App\Models\User;

$user = User::find(1);

// users.first_name => hanako instead of Hanako
$user->first_name = 'Hanako';
```
### Terms
- mutator : 突然変異誘発遺伝子

## Reference
- [Laravel8.x : Eloquent: Mutators & Casting](https://laravel.com/docs/8.x/eloquent-mutators)
