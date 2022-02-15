### What I Learnt

* A route can have a `where` method.
* Laravel has a built in caching mechanism
* Arrow Functions

### `where` method on a route
* A route can have a `where` method to constrain the format of a route parameter.
``` php
Route::get("/posts/{post}", function($slut){
...
})->where('post', '[A-z_\-]+');
```

* The above example restricts the `post` parameters to upper and lowercase alpha characters as well as the dash and underscore. 
* A `post` parameter that doesn't match the where clause will result in a 404.
* In our case `/posts/my-post` would pass but `/posts/my-post2` would result in a 404.
* Helper methods exist for the more common patterns:
- `->whereNumber`
- `->whereAlpha`
- `->whereAlphaNumeric`
- `->whereUUID`

-----
### Laravel has a built in caching mechanism

```php
$post = cache()->remember('posts.{slug}', 5, fn () => file_get_contents($path));
```

---
### Arrow Functions
* ![[Arrow Functions]]

