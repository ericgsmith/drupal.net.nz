#D7 to D8 migration

## Setup

Setup fresh Drupal 8 install using this codebase as per the project [README](../../../../README.md)

Add the drupal 7 database to your `settings.local.php` file using the key **drupal7**

E.g:

```php
$databases['drupal7']['default'] = [
  'database' => 'database_name',
  'username' => 'user',
  'password' => 'password',
  'host' => 'localhost',
  'port' => '3306',
  'driver' => 'mysql',
  'prefix' => '',
  'collation' => 'utf8mb4_general_ci',
];
```

## Run migrations

Ensure this module is enabled then run the migrations via drush.

```
drush migrate-import --all 
```