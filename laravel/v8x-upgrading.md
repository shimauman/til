## Version
- Laravel v8.x

## Models Directory
`app/Models` directory is included by default.

## Model Factory Class
```php
namespace Database\Factories;

use App\Models\User;
use Illuminate\Database\Eloquent\Factories\Factory;
use Illuminate\Support\Str;

class UserFactory extends Factory
{
    /**
     * @var string
     */
    protected $model = User::class;

    /**
     * @return array
     */
    public function definition()
    {
        return [
            'name' => $this->faker->name(),
            'email' => $this->faker->unique()->safeEmail(),
            'email_verified_at' => now(),
            'password' => '$2y$10$92IXUNpkjO0rOQ5byMi.Ye4oKoEa3Ro9llC/.og/at2.uheWG/igi', // password
            'remember_token' => Str::random(10),
        ];
    }
}
```
```php
use App\Models\User;

User::factory()->count(50)->create();
```

### Factory State
```php
/**
 * This state means that the user is suspended.
 *
 * @return \Illuminate\Database\Eloquent\Factories\Factory
 */
public function suspended()
{
    return $this->state([
        'account_status' => 'suspended',
    ]);
}
```

```php
use App\Models\User;

User::factory()->count(5)->suspended()->create();
```

### Use With Relation
```php
$users = User::factory()
            ->hasPosts(3, [
                'published' => false,
            ])
            ->create();
```


## Dump Migration File
We can dump existing migration files into one SQL file.
```
php artisan schema:dump

or

// Delete existing migration files
php artisan schema:dump --prune
```

## Time Test Helper
Test class has some helpers that can change current time.

```php
public function testTimeCanBeManipulated()
{
    // Go to future.
    $this->travel(5)->milliseconds();
    $this->travel(5)->seconds();
    $this->travel(5)->minutes();
    $this->travel(5)->hours();
    $this->travel(5)->days();
    $this->travel(5)->weeks();
    $this->travel(5)->years();

    // Go to past.
    $this->travel(-5)->hours();

    // Go to specific time.
    $this->travelTo(now()->subHours(6));

    // Return to current.
    $this->travelBack();
}
```

## Improve `artisan serve`
`artisan serve` reload automatically when detects changes in `.env` on local.


## Tailwind Pagination View
Paginator use Tailwind CSS framework as default.

## Route Name Space
```php
use App\Http\Controllers\UserController;

Route::get('/users', [UserController::class, 'index']);
```
```php
action([UserController::class, 'index']);

return Redirect::action([UserController::class, 'index']);
```

If we want to set route like before laravel v8.x...
```php
class RouteServiceProvider extends ServiceProvider
{
    protected $namespace = 'App\Http\Controllers';
```

## Reference
- [Laravel readouble : Laravel 8.x Release Notes](https://readouble.com/laravel/8.x/ja/releases.html)
