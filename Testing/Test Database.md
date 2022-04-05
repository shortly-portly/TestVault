To use a test database we first need to define a test connection in `config/database.php`.

WARNING: Always use the same database type in dev, test and production. I've seen tests pass against MYSQL that fail against SQLITE.

```php

  'sqlite_testing' => [
            'driver'                  => 'sqlite',
            'url'                     => env('DATABASE_URL'),
            'database'                => database_path('testing.sqlite'),
            'prefix'                  => '',
            'foreign_key_constraints' => env('DB_FOREIGN_KEYS', true),
        ],
```

Here we have defined a new connection called `sqlite_testing`.

We also need to ensure that the database exists:

```bash
touch database/testing.sqlite
```

Once created we need to run our migrations passing in the name of the new database rather than Laravel using the default.

```bash
php artisan migrate --database sqlite_testing
```

Update `phpunit.xml` to use the new test connection

```xml
        <env name="DB_CONNECTION" value="sqlite_testing"/>
```
