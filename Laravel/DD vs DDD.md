* DD is a Laravel Helper Functions.
* DDD is part of the `Laravel Ignition` package which provides the detailed error page in Laravel apps.
* Both are used for debugging.
* DD stands for Dump and Die
	* Dumps the value of the given variable and ends execution of the script.
	```php
	dd($post)
	```
* DDD stands for Dump, Die, Debug
	* Dumps the value of the given variable and end the execution of the script.
	* Unlike DD, it uses the Ignition Error Page to dispaly its data.
	```php
	ddd($post)
	```
	
	![[images/ddd.png]]