The null coalescing operator (`??`) has been added as syntactic sugar for the common case of needing to use a ternary in conjunction with [isset()](https://www.php.net/manual/en/function.isset.php). It returns its first operand if it exists and is not **`null`**; otherwise it returns its second operand.

```php
<?php  
// Fetches the value of $_GET['user'] and returns 'nobody'  
// if it does not exist.  
$username = $_GET['user'] ?? 'nobody';  
// This is equivalent to:  
$username = isset($_GET['user']) ? $_GET['user'] : 'nobody';  
  
// Coalescing can be chained: this will return the first  
// defined value out of $_GET['user'], $_POST['user'], and  
// 'nobody'.  
$username = $_GET['user'] ?? $_POST['user'] ?? 'nobody';  
?>
```