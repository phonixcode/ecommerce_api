## Application Development Procedures

1. CD into the application root directory with your command prompt/terminal/git bash.

2. Run `cp .env.example .env`.

3. Inside `.env` file, setup database, mail and other configurations.

4. Run `composer install`.

5. Run `php artisan key:generate` command.

6. Run `php artisan migrate:fresh --seed` command.

7. Run `php artisan serve` command.

8. To run a single migration `php artisan migrate --path=/database/migrations/my_migration.php`.

9. To run single seeder `php artisan db:seed --class=ProductSeeder`.

10. `composer require laravel/passport`.

11. Register the service provider inside `config/app.php`. as `Laravel\Passport\PassportServiceProvider::class,`.

12. To generate secure access tokens for your application, Passport requires some encryption keys and two clients known as Laravel Personal Access Client and Laravel Password Grant Client. To create these keys and encryption clients, run the following command: `php artisan passport:install`.

13. If this "Personal access client not found. Please create one. " in Laravel Passport error arises, you can solve it with this command: `php artisan passport:client --personal`.

14. If the error persist, run the following commands
a. `php artisan migrate:fresh --seed`
b. `php artisan config:clear`
c. `php artisan key:generate`
d. `php artisan config:clear`
e. `php artisan passport:install`