## Version
- PHP v8.1

## Enumerations

### < PHP v8.1
```php
class Status
{
    const DRAFT = 'draft';
    const PUBLISHED = 'published';
    const ARCHIVED = 'archived';
}

function acceptStatus(string $status) {}
```

### PHP v8.1
```php
enum Status
{
    case Draft;
    case Published;
    case Archived;
}

function acceptStatus(Status $status) {}

// OK
$status = Status::Draft;
acceptStatus($status);

// TypeError: acceptStatus(): Argument #1 ($status) must be of type Status, string given
pick_a_card('Unpublished');
```

## Readonly Properties

### < PHP v8.1
```php
class BlogData
{
    private Status $status;

    public function __construct(Status $status)
    {
        $this->status = $status;
    }

    public function getStatus(): Status
    {
        return $this->status;
    }
}
```

### PHP v8.1
```php
class BlogData
{
    public readonly Status $status;

    public function __construct(Status $status)
    {
        $this->status = $status;
    }
}

$blogData = new BlogData($status);

// Legal read.
$blogData->status

// Illegal reassignment.
$blogData->status = ***;

// Illegal call.
$blogData::status
```

## New In Initializers

### < PHP v8.1
```php
class Service
{
    private Logger $logger;

    public function __construct(?Logger $logger = null)
    {
        $this->logger = $logger ?? new NullLogger();
    }
}
```

### PHP v8.1
```php
class Service
{
    public function __construct(private Logger $logger = new NullLogger())
    {
        $this->logger = $logger;
    }
}
```

## Pure Intersection Types

### < PHP v8.1
```php
function countAndIterate(Iterator $value) {
    if (!($value instanceof Countable)) {
        throw new TypeError('value must be Countable');
    }

    foreach ($value as $val) {
        echo $val;
    }

    count($value);
}
```

### PHP v8.1
```php
function countAndIterate(Iterator&Countable $value) {
    foreach ($value as $val) {
        echo $val;
    }

    count($value);
}
```

## Never Return Type

### < PHP v8.1
```php
function foo(***) {
    ***
    exit();
}

function bar(***)
{
    ***
    echo 'Hello';
}
```

### PHP v8.1
```php
function foo(***): never {
    ***
    exit();
}

function bar(***): never {
    ***
    echo 'Hello';
}
```

## Final Class Constants

### < PHP v8.1
```php
class Foo
{
    public const XX = "foo";
}

class Bar extends Foo
{
    public const XX = "bar"; // No error
}
```

### PHP v8.1
Final class constants cannot be overridden in child classes.
```php
class Foo
{
    final public const XX = "foo";
}

class Bar extends Foo
{
    public const XX = "bar"; // Fatal error
}
```

## Array Unpacking Support For String-keyed Arrays

### < PHP v8.1
```php
$arrayA = ['a' => 1];
$arrayB = ['b' => 2];

// ['a' => 1, 'b' => 2]
$result = array_merge(['a' => 0], $arrayA, $arrayB);
```

### PHP v8.1
```php
$arrayA = ['a' => 1];
$arrayB = ['b' => 2];

// ['a' => 1, 'b' => 2]
$result = [['a' => 0], ...$arrayA, ...$arrayB];
```


## Reference
- [GitHub php/php-src v8.1.0](https://github.com/php/php-src/blob/php-8.1.0/UPGRADING)
- [PHP official docs : releases v8.1.0](https://www.php.net/releases/8.1/en.php)
- [Qiita :【PHP8.1】PHP8.1がリリースされたので新機能全部やる](https://qiita.com/rana_kualu/items/e350b8ff80f929626eb9)
