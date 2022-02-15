```php
$table->unsignedBigInteger('user_id');
$table->foreign('user_id')->references('id')->on('user')->cascadeOnDelete();
```

is the same as

```php
$table->foreignId('user_id')->constrained()->cascadeOnDelete();
```
