# Virtual hosts
Создаём виртуальные хосты, локальные домены.

- переходим в режим админа `sudo su`
- отключаем сервер, если включен `/opt/lampp/lampp start`

## Папка сайта
В папке `/home/damir/www/` создаём папку `site` здесь разместим файлы сайта.

## hosts
В файле `/etc/hosts` прописываем:

    127.0.0.1   localhost lampp xampp site.test cars.test

## Включаем виртуальные хосты
В файле `/opt/lampp/etc/httpd.conf` раскомментируем строку `Include etc/extra/httpd-vhosts.conf`.

## Создаём виртуальные хосты
В файле `/opt/lampp/etc/extra/httpd-vhosts.conf` прописываем хосты (изменять можно и при работающем сервере, потом его нужно перезагрузить).

Для localhost, чтобы открывалась приветственная страница XAMPP:

    <VirtualHost 127.0.0.1:80>
        ServerAdmin admin@admin.test
        DocumentRoot "/opt/lampp/htdocs"
        ServerName localhost
        ServerAlias 127.0.0.1
    </VirtualHost>

Виртуальный хост в папке `/opt/lampp/htdocs/`, например создаём папку `cars`, в файле прописываем:

    <VirtualHost 127.0.0.1:80>
        ServerAdmin admin@cars.test // можно не писать
        DocumentRoot "/opt/lampp/htdocs/cars/"
        ServerName cars.test
        ServerAlias www.cars.test // можно не писать
    </VirtualHost>

Виртуальный хост в домашней папке `/home/damir/www/`, например создаём папку `site`, в файле прописываем:

    <VirtualHost 127.0.0.1:80>
        ServerAdmin admin@site.test
        DocumentRoot "/home/damir/www/site/"
        ServerName site.test
        ServerAlias www.site.test
        <Directory />
    #       AllowOverride All
            Require all granted
        </Directory>
    </VirtualHost>

Перезагружаем сервер.
