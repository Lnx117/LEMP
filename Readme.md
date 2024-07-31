Для работы скачиваем себе файлы

Затем мы должны установить себе laravel, скачать файлы ларавель в папку src

Делаем с помощью контейнера composer с помощью команды (находясь в папке с проектом)

```
docker compose run --user $(id -u):$(id -g) composer create-project laravel/laravel:^10.0 .
```

Затем также находясь в корне, делаем 
```
sudo chmod -R 777 src
```
Так мы даем права для работы с файлами

Теперь можно открывать папку src и работать там в редакторе, эта папка связана с контейнерами

Для использования artisan выполняем команду, например

```
docker compose run artisan migrate
```

После установки laravel не забываем поменять env на 
```
DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=laravel_db
DB_USERNAME=laravel
DB_PASSWORD=password
```

При поднятом контейнере laravel будет доступен по адресу
http://localhost:8000/

PhpMyAdmin будет доступен по
http://localhost:8080/

Логин laravel
Пароль password