* Start mysql
```
mysql.server start
```

* Enter command line
```
mysql -uroot -p
```

* You will be prompted for the root password.

----

*Some Useful Commands*

* What databases exist?
```sql
show databases;
```

* Create a database

```sql
create database mytodo;
```

* Work with a specific database
```sql
use mytodo;
```

* What tables exist in the current database?
```sql
show tables;
```

* Create a table
```sql
create table todos (
	id integer PRIMARY KEY AUTO_INCREMENT,
	description text NOT NULL, 
	completed boolean NOT NULL);
```

* Show the details of a table (columns)
```sql
describe todos;
```

* Delete a table
```sql
drop table todos;

```

* Insert a row
```sql
insert into todos (description, completed) values('Go to Shop', false);
```

* Show contents of table
```sql
select * from todos;
```
