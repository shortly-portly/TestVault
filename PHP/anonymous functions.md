Anonymous Functions

* An anonymous function is a [[function]] that doesn't have a name.
```php
$my_anonymouse_function = funcion($foo, $bar) {
...
}
```

* Most obvious use case for an anonymous function is as a callback.
```php
$numbers = [1, 2, 3];

$result = array_map(function ($number) {
			return $number + 5;
		  }, $numbers);
```