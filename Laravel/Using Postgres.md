* By default Laravel uses MYSQL.
* To use Postgres, edit the ``.env`` file.
```ruby
DB_CONNECTION=pgsql
DB_HOST=127.0.0.1
DB_PORT=5432
DB_DATABASE=delme
DB_USERNAME=<username>
DB_PASSWORD=<password>
```

* Note you'll need to ensure the database actually exists before running any `migration` commands.