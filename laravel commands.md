composer global require laravel/installer

laravel new myapp       //OR
composer create-project --prefer-dist laravel/laravel myapp  //OR
composer create-project --prefer-dist laravel/laravel myapp 4.2.*
composer create-project laravel/laravel your-project-name 4.2.*
php artisan runserver // to run server




# To create authentication files and related models
php artisan make:auth

#Authentication scaffolding generated successfully.
php artisan make:model Article -m //To crate a model file
php artisan migrate # For migrating models
php artisan migrate:refresh #For refreshing or force migrating models
php artisan make:migration add_paid_to_users # To add another column to table
# Edit your .env and database.php file to avoid errors shon below
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=homestead //laravel_db
DB_USERNAME=homestead //root
DB_PASSWORD=secret // blank


  [Illuminate\Database\QueryException]
  SQLSTATE[HY000] [1045] Access denied for user 'homestead'@'localhost' (using password: YES) (SQL: select * from informatio
  n_schema.tables where table_schema = homestead and table_name = migrations)

  # For creating fake data
  php artisan db:seed --class=ArticlesTableSeeder
