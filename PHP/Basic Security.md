#PHP 

* The following code is dangerous as it allows html tags
```php
<?php
	echo 'Hello, ' . $_GET['name'];
?>
```

Entrying

```
http://localhost:8888/html.php?name=<span=style="color:red">Fred</span>
```

Would return Fred with a font colour of red. 

To prevent this happening wrap any user input in `htmlspecialchars`.

```php
<?php
	echo 'Hello, ' . htmlspecialchars($_GET['name']);
?>
```