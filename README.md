Laravel test for this discussion : https://github.com/laravel/framework/discussions/45570

Create the file : `database/database.sqlite`, then run :

- `composer install`
- `php artisan migrate --seed`
- `php artisan serve`

Then visit http://127.0.0.1:8000/, you can read the files [routes/web.php] and [app/Models/User.php]

What I want :

- Exception thrown when I call `$user->name` (ok)
- Array of attributes *without* `name` when serialization, when I call `$user->toArray()` (ko, the exception is thrown)
