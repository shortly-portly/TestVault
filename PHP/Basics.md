#PHP 

* Double quotes enable interpolation of variables.

```php
$name = 'Dave';

$echo 'Hello $name';
```

will result in 

```
Hello $name
```

But

```php
$name = 'Dave';

$echo "Hello $name";
```

will result in

```
Hello Dave
```

----

* Shortcut for `echo`

```php
<?= 'Hello, ' . $_GET['name']; ?>
```

is a shortcut for

```php
<?php
	echo 'Hello, ' . $_GET['name'];
?>
```