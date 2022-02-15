* An Arrow Function provides a more precise syntax for [[anonymous functions]].

```php
    $post = cache()->remember('posts.{slug}', 5, fn () => file_get_contents($path));
```

* Using variables from the parent scope is automatic.
* 