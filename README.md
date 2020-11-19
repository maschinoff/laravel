# Dockerized laravel

## Usage 

```bash
cd docker
docker-compose up -d
docker-compose run --rm composer composer create-project --prefer-dist laravel/laravel .
docker-compose exec php-fpm php artisan key:generate
docker-compose exec php-fpm php artisan migrate
```

Laravel app is available on [http://127.0.0.1](http://127.0.0.1).

Make sure you configured services correctly in the `.env` file.

DB_CONNECTION=mysql
DB_HOST=db
DB_PORT=3306
DB_DATABASE=laravel
DB_USERNAME=user
DB_PASSWORD=secret

## Useful links
- [Adminer](http:///127.0.0.1:8082)  
- [Laravel docs](https://laravel.com/docs/8.x/installation)
